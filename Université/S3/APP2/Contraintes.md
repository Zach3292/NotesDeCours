### Règles d'un système d'équations dynamiques
Pour former un système d'équations représentant la dynamique d'un corps, il faut respecter deux lois:
$$p=n-m$$
Où
- $p$: le nombre de degrés de liberté
- $n$: le nombre de variable de mouvement
- $m$: le nombre de contrainte *scalaire*
Et:
$$nE=nI$$
Où
- $nE$: le nombre d'équation (équation de mouvement *EOM* et équation de contrainte *EOC*)
- $NI$: le nombre d'inconnu (variable de mouvement, force de réaction)

Il faut toujours que ces deux équations soient vrai pour former un système d'équations.

**Pour un même système, $p$ est constant même si $n$ et $m$ varient selon la façon qu'on modélise le système.**

### Type de contrainte

#### Corde, tige et séparateur
Limite un axe de translation
##### Corde de longueur $L_n$
$$\vec{r}^{Q/O}\cdot\vec{r}^{Q/O}\leq L_n^2$$
##### Tige de longueur $L_n$
$$\vec{r}^{Q/O}\cdot\vec{r}^{Q/O}= L_n^2$$
##### Séparateur de longueur $L_n$
$$\vec{r}^{Q/O}\cdot\vec{r}^{Q/O}\geq L_n^2$$
#### Actuateur linéaire
Limite un axe de translation
##### Distance $d$
$$\vec{r}^{Q/O}\cdot\vec{r}^{Q/O}= d^2$$
##### Élongation $\dot{d}$
$$\vec{r}^{Q/O}\cdot\frac{^Fd\vec{r}^{Q/O}}{dt}=d\dot{d}$$
##### Dérivée de l'élongation $\ddot{d}$
$$\vec{r}^{Q/O}\cdot\frac{^Fd^2\vec{r}^{Q/O}}{dt}+\frac{^Fd\vec{r}^{Q/O}}{dt}\cdot\frac{^Fd\vec{r}^{Q/O}}{dt}=d\ddot{d}+\dot{d}^2$$
#### Rotule
Limite trois axes de translation
$$\vec{r}^{B_A/A_B}=\vec{0}$$
#### Penture
Limite trois axes de translation et deux axes de rotation
$$\vec{r}^{B_A/A_B}=\vec{0}$$
$$\hat{a_x}\times\hat{b_x}=\vec{0}$$
#### Joint prismatique
Limite deux axes de translation et trois axes de rotations
$$^A\vec{\omega}^B=\vec{0}$$
Si les bases des deux corps sont alignées:
$$\vec{r}^{B_A/A_B}\cdot\hat{t_i}=0 \ \ \ \textrm{ (i=y,z)}$$

#### Roulement et glissement
##### Roulement
$$^F\vec{v}^{B_A}\triangleq{}^F\vec{v}^{A_B}$$
##### Glissement
$$^F\vec{v}^{B_A}\neq{}^F\vec{v}^{A_B}$$

