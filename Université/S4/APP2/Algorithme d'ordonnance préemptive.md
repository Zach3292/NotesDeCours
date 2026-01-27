Lorsqu'un système temps réel n'est pas purement réactif il aura des tâches périodiques, pour superviser l'état du système. Les algorithme d'ordonnance devront prédire ces tâches et les inclure dans leur ordre d'exécution. On dit de ces algorithmes qu'ils sont prédictif.

### Ligne de temps
Comme pour [l'ordonnance non-prédictif](Algorithme%20d'ordonnance%20non-préemptive.md), il est possible de produire un ordre d'exécution manuellement. Cependant, cette méthode est seulement valable lorsqu'il y a un petit nombre de tâche. Sinon, le travail devient rapidement herculéen et impossible pour une personne à réaliser. Cette méthode peut être utile pour essayer de réduire le nombre de [changement de contexte](../../S3/APP6/Programmation%20concurrente.md). 
#### Problème de la ligne du temps
Imaginons qu'on a réussi à créer un ordre d'exécution fonctionnelle pour nos tâches périodiques et qu'on essaye notre système en temps réel. Qu'arrive-t-il quand des tâches sporadiques doivent s'exécuter? Comment choisir qu'elle tâche sacrifier? Dans des systèmes complexes, des tâches peuvent apparaître au moment de l'exécution sans qu'on puisse les prédire. 

Un autre problème est que l'horaire doit être recalculer au complet dès qu'une nouvelle tâche arrivent.

### Classement de priorité
Une alternative pour ordonnée les tâches est d'assigné à chaque tâche une priorité. En général cette priorité se situe entre 0 et 255 où le plus petit nombre est le plus prioritaire. Les priorités peuvent être fixe ou dynamique. Les tâches les plus prioritaires vont être exécutées en premier dans la liste d'attente.

#### Variabilité (Jitter)

Lorsqu'une tâche de basse priorité à une longue période, il y a un risque qu'elle ne puisse pas être exécuter comme elle devrait puisqu'elle se fait toujours interrompre. Ainsi, plus la priorité est basse, plus la variabilité de la tâche est haute. 

