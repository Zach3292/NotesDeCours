### Définition
Il s'agit d'une programmation où deux ou plus actions s'exécutent en parallèle. Cela permet des opérations plus efficaces et rapides: ![](Pasted%20image%2020250711075808.png)

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