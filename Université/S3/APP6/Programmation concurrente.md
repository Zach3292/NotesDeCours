### Définition
Il s'agit d'une programmation où deux ou plus actions s'exécutent en parallèle. Cela permet des opérations plus efficaces et rapides:
![parallele](parallele.png)

On peut rouler un programme par fil *thread* en même temps avant de devoir alterner les tâches comme sur un seul fil. Ainsi, plus un ordinateur à de *thread*, plus il peut exécuter d'applications en parallèle.

### Lancer un fil
Il est très simple de lancer un fil en C++. Voici un exemple:
```cpp
void do_something();
std::thread my_thread(do_something);
```
On peut ensuite choisir d'attendre que le fil finisse (le joindre) ou on peut se détacher du fil pour continuer de faire autres choses:
```cpp
void do_something();
void do_somehting_else();
std::thread my_thread(do_something);
std::thread my_other_thread(do_something_else);

my_thread.detach();
my_other_thread.join();
```
Il faut absolument rejoindre ou se détacher d'un fil avant que celui-ci soit détruit.

### Partage de ressources
Lorsque plusieurs fils essayent de faire autre chose que seulement lire une même information dans la mémoire partagée, il y a un problème.

#### Concurrence critique (race condition)
Quand le résultat d'une opération dépend de la vitesse relative d'un fil par rapport à un autre. En d'autre mots, quand le résultat dépend de l'ordre d'exécution des opérations dans plusieurs fils.
#### Mutex
La manière la plus simple de protéger notre code contre les concurrences critiques est d'utiliser des *mutex*. Il s'agit de drapeau forçant [[l'atomicité|#l'atomicité]] d'un code. Ça permet de mettre un verrou sur une séquence ou une variable. Ainsi, un code essayant de prendre possession du verrou si celui-ci est déjà barré ne pourra pas et devra attendre. 

Avant d'accéder à de l'information partagée, on verrouille le mutex associé et lorsqu'on a fini avec l'information, on déverrouille le mutex. Il faut cependant faire attention puisque parfois, l'accès a un pointeur vers de l'information pourrait contourner le mutex et la protection. Voici comment faire un mutex de base en C++:
```cpp
#include <mutex>
#include <list>
#include <algorithm>

std::list<int> some_list;
std::mutex some_mutex;

void add_to_list(int new_value)
{
	std::lock_guard<std::mutex> guard(some_mutex);
	some_list.push_back(new_value);
}

void list_contains(int value_to_find)
{
	std::lock_guard<std::mutex> guard(some_mutex);
	return std::find(some_list.begin(), some_list.end(), value_to_find) != some_list.end();
}
```

##### Deadlock
Il s'agit d'un problème avec les mutex qu'au lieu d'avoir deux fils qui essayent d'accéder à la même information en même temps, il y a deux fils qui attendent un après l'autre pour le déverrouillage d'une information. Ils vont donc attendre à l'infini dans ce qu'on appelle un *deadlock*. Pour régler ce problème, il faut toujours verrouiller les mutex dans le même ordre. 

Une autre solution existe en C++ pour prendre possession de deux mutex sans risque de deadlock:
```cpp
std::lock(mutex1, mutex2);
```
Cette fonction permet soit de verrouiller les deux mutex, ou d'en verrouiller aucun, il n'y a pas d'entre deux. Il faut ensuite transférer la possession du verroux vers le lock_guard pour qu'il se déverrouille automatiquement:
```cpp
std::lock(mutex1, mutex2);
std::lock_guard<std::mutex> lock1(mutex1, std::adopt_lock);
std::lock_guard<std::mutex> lock2(mutex2, std::adopt_lock);
```

### Synchronisation des opérations parallèles
Pour pouvoir synchroniser plusieurs fils ensemble, on peut utiliser des variables de condition. Un fil attend un notification et l'autre fil l'envoie. Pendant ce temps, le fil qui attend est au repos et ne prend pas de performance pour vérifier un drapeau. Une variable de condition doit être associée à un mutex pour bien fonctionner. Il est important de le créer avec un *unique_lock* au lieu d'un *lock_guard* pour pouvoir les déverrouiller au besoin.
```cpp
#include <cstdio>
#include <thread>
#include <mutex>
#include <queue>
#include <cstdlib>      // rand
#include <condition_variable>

namespace {
    std::queue<int> queue_;
    std::mutex      mutex_;
    std::condition_variable notifier;
}

void add_to_queue(int v)
{
    // Fournit un accès synchronisé à queue_ pour l'ajout de valeurs.
    
    std::lock_guard<std::mutex> lock(mutex_);
    queue_.push(v);
    notifier.notify_one();
}

void prod()
{
    for (int i = 0; i < 100; ++i)
    {
        int r = rand() % 1001 + 1000;
        add_to_queue(r);

        // Bloque le fil pour 50 ms:
        std::this_thread::sleep_for(std::chrono::milliseconds(50));
    }

    add_to_queue(0);
}

void cons()
{
    while (true)
    {
        std::unique_lock<std::mutex> lock(mutex_);
        notifier.wait(lock, []{return !queue_empty();});
        // On doit toujours vérifier si un objet std::queue n'est pas vide
        // avant de retirer un élément.
        if (!queue_.empty()) {
            int v = queue_.front(); // Copie le premier élément de la queue.
            queue_.pop();           // Retire le premier élément.
			lock.unlock();
            printf("Reçu: %d\n", v);
        }
    }

}

int main()
{
    std::thread t_prod(prod);
    std::thread t_cons(cons);

    t_prod.join();
    t_cons.join();

    return 0;
}
```
#### Retour de valeur de tache en arrière plan
Il est possible de retourner une valeur pour une fonction qui s'exécute en arrière plan. D'autres actions sont possible en parallèle et on peut ensuite attendre d'obtenir le résultat initial.
```cpp
#include <future>
int fonction_a_retour(int argument);
void autre_chose();
int main()
{
	std::future<int> reponse=std::async(fonction_a_retour, argument);
	autre_chose();
	reponse.get(); // Attend le retour ici
}
```
### Opérations atomiques
Une opération atomique est une opération indivisible, qui doit toujours s'exécuter au complet avant de pouvoir passer à autre chose. Il s'agit d'une caractéristique importante lors de la parallélisation de code. Si on doit faire une opération sur une variable et que l'on ne veut pas que cette opération soit diviser par un *context switch*.

### Multi-fil vs multi-processus

| Fil                                                                    | Processus                                                                                      |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Accès à la mémoire du processus                                        | Pas accès à la mémoire du processus                                                            |
| Très rapide écrire dans la mémoire                                     | Doit utiliser un autre procédé pour écrire dans la mémoire partagé (tuyau, fichier temporaire) |
| Section critique de mémoire (deux fils accèdent à la même information) | Nécessité de copier la mémoire (en c++), plus lent                                             |
| Doit ajouter des mécanismes de synchronicité                           |                                                                                                |
| Mutex, variable de condition, atomique, future                         | Sémaphore (gérer par l'OS)                                                                     |
|                                                                        |                                                                                                |
