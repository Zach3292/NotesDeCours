### Définition
Une équation différentielle est une équation de forme $G(x, y, y', ...)=0$ où $G$ est une fonction quelconque. On définit:
- $x$ une variable **indépendante**
- y(x) une variable **dépendante**, c'est la solution que l'on cherche à déterminer

On suppose souvent qu'il est possible d'isoler la dérivée d'ordre le plus élevé pour modifier l'équation originale.

#### Ordre
L'ordre d'un équation différentielle est l'ordre de la plus haute dérivée présente dans l'équation

#### Problème aux valeurs initiales
Consiste à chercher une solution selon certaine condition initiale
#### Équations différentielles linéaires
Respecte les descriptions vues [ici](../../S1/APP6/Équations%20différentielles%20linéaires%20du%20premier%20et%20second%20ordre.md#Équation%20différentielle%20linéaire). 

##### À coefficients constants
Comme vu [ici](../../S1/APP6/Équations%20différentielles%20linéaires%20du%20premier%20et%20second%20ordre.md#Équation%20linéaire%20différentielle%20à%20coefficients%20constants).

### Méthode de résolution d'équations différentielles
On utilise trois étapes pour résoudre l'équation suivante: $$y(x)=y_0 + \int_{x_0}^x{y'(l)dl}=y_0 + \int_{x_0}^x{F(l,y(l))dl}$$
#### La discrétisation
Comme pour une intégrale numérique:
$$h=\frac{x-x_0}{n}$$
$$y_0=y(x_0)$$
$$y_{k+1}=y_k+I_k$$
avec $$I_k=\int_{x_k}^{x_k+1}{F(y(l),l)dl}$$
#### La méthode d'intégration numérique
Sur chaque intervalle on utilise la méthode [d'intégration numérique](Différentiation%20et%20intégration%20numérique.md#Intégration%20numérique) de notre choix. 

#### L'approximation de $y(l)$ sur chaque intervalle
Les méthodes d'intégrations numérique repose sur une approximation de $y(l)$ sur chaque intervalle, plus $h$ est petit, plus l'approximation sera bonne

### Schémas numériques d'intégration des ODEs
#### Méthode d'Euler (Runge-Kutta d'ordre 1)
Il s'agit d'utiliser la méthode des rectangles pour approximer l'intégrale. L'erreur sera donc proportionnelle à $h$. En réduisant $h$ d'un facteur 10, on diminue l'erreur de facteur 10. La méthode est donc d'ordre 1.

Il y a une certaine convergence, plus $h$ est petit, plus l'erreur converge vers 0.

C'est aussi la méthode qui demande le moins de calcul par intervalle, donc la plus rapide pour un nombre d'intervalle $n$ donné.

pour $k=0$: $y_0=y(x_0)$

Pour tout $k > 0$: $k_1=hF(y(x_k),x_k)$ et $y_{k+1}=y_k+k_1$.
#### Méthode de Heun (Runge-Kutta d'ordre 2)
La convergence de la méthode d'Euler est généralement trop lente en pratique. On peut donc utiliser la méthode des trapèzes pour réduire l'erreur pour un même nombre d'intervalle.