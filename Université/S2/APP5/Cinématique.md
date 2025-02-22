Elle consiste à calculer les fonctions de transformations pour passer d'un système de coordonnées à un autre.

### 3.1 Systèmes de coordonnées
Un système de coordonnées est un ensemble de scalaires, généralement des distances et des angles qui décrivent la position d'un système.
#### 3.1.1 Position d'une particule
Dans un espace 3D, un particule à 3 DDL. On peut utiliser trois types de systèmes pour la décrire:
1. Cartésien
2. Cylindrique
3. Sphérique
![systeme](Images/systemes.png)
Selon la situation, un système peut être plus adapté qu'un autre. Voici une charte de conversion d'un système à l'autre:

|                  | De cartésien                                                                                           | De cylindrique                                                         | De sphérique                                                                           |
| ---------------- | ------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Vers cartésien   | $x=x$<br>$y=y$<br>$z=z$                                                                                | $x=r\cos{\theta}$<br>$y=r\sin{\theta}$<br>$z=z$                        | $x=\rho\sin{\phi}\cos{\theta}$<br>$y=\rho\sin{\phi}\cos{\theta}$<br>$z=\rho\cos{\phi}$ |
| Vers cylindrique | $r=\sqrt{x^2+y^2}$<br>$\theta=\arctan{\frac{y}{x}}$<br>$z=z$                                           | $r=r$<br>$\theta=\theta$<br>$z=z$                                      | $r=\rho\sin{\phi}$<br>$\theta=\theta$<br>$z=\rho\cos{\phi}$                            |
| Vers sphérique   | $\rho=\sqrt{x^2+y^2+z^2}$<br>$\theta=\arctan{\frac{y}{x}}$<br>$\phi=\arctan{\frac{\sqrt{x^2+y^2}}{z}}$ | $\rho=\sqrt{r^2+z^2}$<br>$\theta=\theta$<br>$\phi\arctan{\frac{r}{z}}$ | $\rho=\rho$<br>$\theta=\theta$<br>$\phi=\phi$                                          |

#### 3.1.2 Pose d'un corps rigide
Dans un système 3D, la position d'un corps rigide à 3 DDL et sa rotation aussi. Ainsi, On peut représenté sa position et son orientation avec des systèmes à 6 DDL. On appelle cette information la **pose** d'un corps rigide. Il existe plusieurs manières de représenter l'orientation d'un corps rigide et il s'agit d'un problème complexe. On peut utiliser des matrices de rotations, des angles d'Euler ou des quaternions. Ces méthodes seront discuté à la section [3.7](#3.7).
#### 3.1.3 Configuration d'un robot manipulateur
On appelle un ensemble de variables indépendantes qui permet de déterminer la configuration d'un robot des *coordonnées généralisées*. Le nombre de coordonnées correspond au nombres de DDL. 

On utilise généralement deux types de systèmes de coordonnées en robotique:
##### Espace des joints/actionneurs
Chaque coordonnées de ce système correspond à une mesure locale d'une DDL qui relie deux liens rigides. Elles correspondent au déplacement relatif de chaque joint.
##### Espace de la tâche
L'espace de la tâche est souvent définit en terme de coordonnées cartésienne de l'effecteur qui effectue la tâche.
### 3.2 Approche dans ce chapitre
On utilise une approche précise dans ce chapitre pour modéliser des systèmes:
1. Décrire le problème avec des vecteurs géométriques symboliques
2. Choisir des bases appropriées
3. Traduire la relation vectorielle en relation matricielle (projection dans une base)
4. Déterminer la solution numérique avec les outils de l'algèbre linéaire
### 3.3 Vecteurs géométriques de positions

### 3.7