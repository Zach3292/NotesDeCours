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

#### Apériodique
Une tâche apériodique est une tâche qui s'exécute à un interval irrégulier. Il n'y a pas de minimum entre deux exécutions. Généralement c'est tâches ne peuvent pas être [*hard real-time* ou *firm real-time*](Introduction%20au%20système%20temps%20réel.md#Classement%20des%20systèmes).

#### Sporadique
Une tâche sporadique est comme une tâche apériodique