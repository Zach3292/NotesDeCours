### Définition
L'ordonnance *(scheduling)* est l'action d'exécuter des tâches dans un ordre précis pour prioriser certaines d'entres elles qui sont plus importantes. Dans des systèmes en temps réel, il n'est pas toujours possible d'exécuter plusieurs tâches en même temps, il faut donc déterminer l'ordre de priorité d’exécution des tâches.

### Classification des tâches
On peut décrire une tâche selon comment souvent elle s'exécute et combien de temps elle nécessite pour s'exécuter.

Un tâche peut être plusieurs choses:
- *Processor bound*: lorsque la ressource limite est le temps de processeur
- *Memory bound*: lorsque la ressource limite est l'accès à la mémoire
- *I/O bound*: lorsque la ressource limite est un autre facteur que le processeur ou la mémoire. (Attendre après l'utilisateur, un autre appareil, etc.)

On divise les tâches en quatre catégories:
1. Instance fixe
2. Périodique
3. Apériodique
4. Sporadique

#### Instance fixe
Il s'agit d'une tâche qui s'exécute un nombre fini de fois, souvent une seule. 

#### Périodique
Une tâche périodique est une tâche qui doit être exécuter selon un temps de cycle fixe, par exemple, à toutes les secondes. Il est important de prendre en compte le temps que prend une tâche périodique à s'exécuter pour ne pas qu'elle occupe tout le temps de processeur.

##### Super période
Plus petit commun multiple entre toutes les tâches périodiques.

#### Apériodique
Une tâche apériodique est une tâche qui s'exécute à un interval irrégulier. Il n'y a pas de minimum entre deux exécutions. Généralement c'est tâches ne peuvent pas être [*hard real-time* ou *firm real-time*](Introduction%20au%20système%20temps%20réel.md#Classement%20des%20systèmes). Elles sont **parfaitement imprévisible**.

#### Sporadique
Une tâche sporadique est comme une tâche apériodique mais qui requière habituellement un *hard ou firm real-time*. Les tâches sporadiques par leur nature peuvent occuper tout le temps de processeur pendant un moment. Il faut alors décider de la priorité des tâches. Lorsque ces tâches sont prêtes à rouler, elles sont traités comme des tâches périodiques. Pour pouvoir exécuter les tâches sporadiques, il est nécessaire qu'il y ait un interval minimal entre celle-ci pour laisser le tempos au processeur de les gérer.

### Estimation du pire temps d'exécution (WCET)
Avant de pouvoir savoir si un algorithme d'ordonnance pourra permettre à toutes les tâches de satisfaire leur limite de temps, il faut savoir le temps d'exécution de chaque tâche. Comme le temps d'exécution peut varier, il faut estimer le pire temps d'exécution possible pour chaque tâche *(worst-case execution time WCET)*. En utilisant ce pire temps, on peut ensuite analyser si chaque tâche pourra être exécuter selon sa limite de temps.

Il existe deux manières d'estimer le WCET:
1. L'analyse du code source
	1. Tendance à surestimer à cause des optimisations du compilateur
	2. Si notre analyse est concluante, on est sur que ça fonctionne car elle est pessimiste
2. L'estimation à partir des données empiriques
	1. Très simple à faire

### Le fil en attente (idle)
Lorsqu'il n'y a aucune tâche à exécuter, le fil doit être mis en attente. Un fil en attente peut faire plusieurs choses différentes. La solution la plus simple serait de mettre le processeur en veille pendant ce temps. Une autre solution serait d'effectuer des calculs qui ne dépendent pas de ressources précises. Ainsi, on utilise du temps de processeur qui serait autrement gaspillé. L'important est que cette tâche du fil en attente soit seulement exécuter lorsqu'il n'y a aucune autre tâche nécessaire. Il s'agit de la tâche avec la plus basse priorité.

### Ordonnance préemptive vs non-préemptive
- Un [ordonnateur préemptif](Algorithme%20d'ordonnance%20préemptive.md) **est appelé à une période fixe** pour s'exécuter.
- Un [ordonnateur non-préemptive](Algorithme%20d'ordonnance%20non-préemptive.md) doit **être appelé par la tâche** elle même pour s'exécuter.