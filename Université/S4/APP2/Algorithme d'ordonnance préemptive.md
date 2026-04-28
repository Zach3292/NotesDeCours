Lorsqu'un système temps réel n'est pas purement réactif, il aura des tâches périodiques pour superviser l'état du système. Les algorithmes d'ordonnance devront prédire ces tâches et les inclure dans leur ordre d'exécution. On dit de ces algorithmes qu'ils sont prédictifs.

### Ligne de temps
Comme pour [l'ordonnance non-préemptive](Algorithme%20d'ordonnance%20non-préemptive.md), il est possible de produire un ordre d'exécution manuellement. Cependant, cette méthode est seulement valable lorsqu'il y a un petit nombre de tâches. Sinon, le travail devient rapidement herculéen et impossible pour une personne à réaliser. Cette méthode peut être utile pour essayer de réduire le nombre de [changements de contexte](../../S3/APP6/Programmation%20concurrente.md). 
#### Problème de la ligne du temps
Imaginons qu'on a réussi à créer un ordre d'exécution fonctionnelle pour nos tâches périodiques et qu'on essaie notre système en temps réel. Qu'arrive-t-il quand des tâches sporadiques doivent s'exécuter? Comment choisir quelle tâche sacrifier? Dans des systèmes complexes, des tâches peuvent apparaître au moment de l'exécution sans qu'on puisse les prédire. 

Un autre problème est que l'horaire doit être recalculé au complet dès qu'une nouvelle tâche arrive.

### Classement de priorité
Une alternative pour ordonner les tâches est d'assigner à chaque tâche une priorité. En général cette priorité se situe entre 0 et 255 où le plus petit nombre est le plus prioritaire (freeRTOS utilise un système de priorité à 32 valeurs avec 31 = configMAX_PRIORITIES  et 0 = tskIDLE_PRIORITY). Les priorités peuvent être fixes ou dynamiques. Les tâches les plus prioritaires vont être exécutées en premier dans la liste d'attente.

#### Tâche de même priorité
Si toutes les tâches ont la même priorité, l'ordonnateur va changer de tâche à chaque tick dans un *round-robin*.

#### Variabilité (Jitter)
La variabilité est la différence du moment de fin d'une tâche d'une exécution à l'autre. Elle est influencée majoritairement par l'intéruption de l'exécution par d'autres tâches. 

Lorsqu'une tâche de basse priorité a une longue période, il y a un risque qu'elle ne puisse pas être exécutée comme elle devrait, puisqu'elle se fait toujours interrompre. Ainsi, plus la priorité est basse, plus la variabilité de la tâche est haute. 

Variabilité sur le temps de fin d'une tâche périodique.

### Inversion et héritage de priorité

Problème: inversion de priorité avec un mutex -> Solution: héritage de priorité.