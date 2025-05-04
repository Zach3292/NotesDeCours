### Définition
La vitesse est la dérivée de la position. On définie la vitesse d'un point $Q$ dans un référentiel inertiel $N$ comme suit:
$$^N\vec{v}^Q\triangleq \frac{^Nd(\vec{r}^{Q/N_O})}{dt}$$
On peut aussi définir l'accélération du même point dans le même référentiel comme suit: 
$$^N\vec{a}^Q\triangleq \frac{^Nd(^N\vec{v}^Q)}{dt}$$
**Un point peut avoir une vitesse mais pas un corps.** *Sauf pour les situations où tous les points du corps on la même vitesse(très rare).*

### Simplification pour certain cas
Si on a deux points $Q$ et $B_O$ fixes dans un référentiel, on peut calculer la vitesse et l'accélération de $Q$ dans $N$ à partir de la vitesse, l'accélération et la position de $B_O$ dans $N$. 
$$^N\vec{v}^Q= {}^N\vec{v}^{B_O}+{}^N\vec{\omega}^B\times\vec{r}^{Q/B_O}$$
$$^N\vec{a}^Q= {}^N\vec{a}^{B_O}+{}^N\vec{\alpha}^B\times\vec{r}^{Q/B_O}+{}^N\vec{\omega}^B\times\left({}^N\vec{\omega}^B\times\vec{r}^{Q/B_O}\right)$$
### Vocabulaire d'accélération
L'équation complète de l'accélération par rapport à un référentiel $N$ d'une particule $Q$ qui bouge sur un corps rigide $B$ est la suivante:
$$^N\vec{a}^Q= {}^N\vec{a}^{B_O}+{}^N\vec{\alpha}^B\times\vec{r}^{B_Q/B_O}+{}^N\vec{\omega}^B\times\left({}^N\vec{\omega}^B\times\vec{r}^{B_Q/B_O}\right)+{}^B\vec{a}^Q+2{}^N\vec{\omega}^B\times{}^B\vec{v}^Q$$
Où
- $^N\vec{a}^Q$: L'accélération de $Q$ dans $N$
- $^N\vec{a}^{B_O}$: L'accélération de $B_O$ dans $N$
- $^N\vec{\alpha}$: L'accélération angulaire de $B$ dans $N$
- $^N\vec{\alpha}^B\times\vec{r}^{B_Q/B_O}$: L'accélération tangentielle de $Q$ sur $B$ dans $N$
- $^N\vec{\omega}^B\times\left({}^N\vec{\omega}^B\times\vec{r}^{B_Q/B_O}\right)$: L'accélération centripète de $Q$ sur $B$ dans $N$
- $^B\vec{a}^Q$: L'accélération de $Q$ dans $B$
- $2{}^N\vec{\omega}^B\times{}^B\vec{v}^Q$: L'accélération de Coriolis de $Q$ sur $B$ dans $N$.