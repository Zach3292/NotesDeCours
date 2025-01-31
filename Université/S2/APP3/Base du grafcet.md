L'exécution d'un programme grafcet se fait en trois étapes: la lecture des nouvelles valeurs en entrée, l’exécution du programme et la mise à jour des sorties.

Un grafcet est une programmation d'une [machine à état](../Projet/Machine%20à%20état.md). Il respecte donc le [principe d'automaintien](../Projet/Machine%20à%20état.md#Principe%20d'auto-maintien). Il est possible de faire du grafcet en diagramme à échelle mais il est beaucoup plus simple d'utilisé un langage plus graphique tel que le **SFC**. ![sfc](Images/sfc.png)
Dans du **SFC**, on peut inclure des la logiques non-booléenne. Il s'agit de texte structuré. Il est **important** de noté la différence entre les deux symboles d'assignation de variable en texte structuré. Le symbole **:=** est une assignation normale d'une variable tandis que le symbole **[:=]** est une assignation temporaire. La variable va revenir à son état initiale lorsque l'état va être fini.
#### Parallélisme
Même si mathématiquement un machine à état ne peut pas avoir plusieurs états de sortie, il est possible de faire du parallélisme en **SFC**.

#### Hiérarchie de grafcet
On ne réalise pas tout dans le même grafcet. Il est d'usage de séparé les taches dans différents programmes. Cependant, il y a un ordre de priorité:
1. Gr