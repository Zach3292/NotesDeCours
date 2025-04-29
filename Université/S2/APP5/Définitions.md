### 2.1 Mécanismes et composants
#### 2.1.1 Liens rigides
Un ensemble de pièce fixes les unes par rapport aux autres qui forment un corps rigide. Aucun mouvement relatif possible entre ces pièces.
#### 2.1.2 Joints
Les articulations d'un robot. Un **joint prismatique** permet la translation selon un axe entre deux pièces et un **joint rotatif** permet à deux pièces de pivoter relativement à un axe. La variable $q_i$ utilisée pour décrire la configuration d'un joint $i$ est un distance *m* pour un joint prismatique et un angle *rad* pour un rotatif.

Chaque joint représente un degré de liberté *DDL* pour le robot. Des joints plus complexes comme un joint sphérique peuvent ajouter plus d'un DDL.
#### 2.1.3 Effecteur
L'effecteur représente l'outil du robot, par exemple un fer à souder, un pointeur ou une caméra. Dans un espace tri-dimensionnel, la position de l'effecteur est décrite par six variables. Il a donc 6 DDL.
#### 2.1.4 Actionneur
Ils sont les *muscles* du robot, les moteurs et actuateurs qui lui permet de bouger.
#### 2.1.5 Capteurs
Les dispositifs qui collectent de l'information sur l'état interne du robot, par exemple un encodeur rotatif.
### 2.2 Configurations
#### 2.2.1 Degrés de liberté DDL
Ça représente le nombre de variable nécessaire pour décrire la configuration ou l'état d'un mécanisme. Si le nombre de DDL du robot est supérieur à celui de l'Effecteur, le robot est dit **redondant**.
#### 2.2.2 Espace de travail
Il s'agit du volume formé de la combinaison de toute les positions atteignables par l'effecteur robot.