Le lien entre la vitesse angulaire de chaque joint et la vitesse linéaire de l'effecteur
### 4.1 Référentiel
Il s'agit d'un solide ou un ensemble de points par rapport auquel un observateur qui mesure un mouvement est fixe. Le choix d'un référentiel influence "la physique" du problème.
#### 4.1.1 Référentiel vs repère
un référentiel est un point de vue utilisé pour décrire un phénomène, une origine est un point par rapport auquel les mesures de position sont faites et une base vectorielle représente l'orientation du système d'axe utilisé. On peut choisir ces trois éléments indépendamment. On fait ensuite un repère avec l'origine et la base.

Un repère sert à définir une *position par rapport à quoi* tandis qu'un référentiel sert à définir une *vitesse par rapport à quoi*.

Un changement d'**origine** correspond à une **translation** du mouvement. 

Un changement de **base** correspond à une **rotation** du mouvement. 

Un changement de **référentiel** correspond à une **dilatation** du mouvement.
### 4.2 Vitesse et dérivée d'un vecteur position
Un vecteur de vitesse est défini comme la dérivée temporelle du vecteur de position:
$$\vec{v}_{B/A}=\frac{d}{dt}\vec{r}_{B/A}$$
Pour avoir la vitesse d'un point $B$, il faut:
1. Que le dérivée soit faite par rapport à une base fixe dans un référentiel inertiel
2. Que le vecteur position dérivé soit par rapport à une origine fixe dans un référentiel inertiel

Le vecteur vitesse est donc définit par un seul point contrairement au vecteur position.

Si:
$$\vec{r}_{B/A}=x\hat{a}_1+y\hat{a}_2+z\hat{a}_3$$
Alors
$$\vec{v}_{B/A}=\frac{d}{dt}\vec{r}_{B/A}=\dot{x}\hat{a}_1+\dot{y}\hat{a}_2+\dot{z}\hat{a}_3$$
#### 4.2.1 Dérivée d'un vecteur position exprimé avec une base mobile.
*Pour cette section, les repères $A$ sont fixes et $B$ sont mobiles*

Si on connait les composantes d'un vecteur position dans un base mobile $b$:
$$\vec{r}_{B/A}=x\hat{b}_1+y\hat{b}_2+z\hat{b}_3$$
Alors lorsqu'on dérive par rapport au temps, il faut prendre compte du mouvement du repère $B$ dans le temps aussi:
$$\vec{v}_{B/A}=\frac{d}{dt}\vec{r}_{B/A}=\dot{x}\hat{b}_1+\dot{y}\hat{b}_2+\dot{z}\hat{b}_3+x\dot{\hat{b}}_1+y\dot{\hat{b}}_2+z\dot{\hat{b}}_3$$
Il y a donc deux sources de contribution au vecteur vitesse, le taux de variation des composantes et le taux de variation de la direction des vecteurs unitaires. La dérivée temporelle des vecteur unitaire est directement relié à la vitesse angulaire de la base $b$. On peut calculer la contribution de ce mouvement avec un produit vectoriel:
$$\vec{v}_{B/A}=\frac{d}{dt}\vec{r}_{B/A}+\vec{\omega}_{b/a}\times\vec{v}_{B/A}$$
Où $b$ est une base mobiel et $a$ est une base fixe dans le référentiel interiel