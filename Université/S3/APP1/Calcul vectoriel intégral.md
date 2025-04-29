### Fonction vectorielle
Elle est défini comme un vecteur de l'Espace dont les composantes dépendent de la variable $t$.
#### Dérivation
Les mêmes [règles](../../../Collégial/1ere%20session/Math/Base%20de%20la%20dérivée.md#Définition) que pour une fonction réelle s'applique aux fonctions vectorielles.

### Courbes dans l'espace et mesures

On peut utiliser des fonctions vectorielles pour décrire des courbes dans l'espace. 
#### Tangente d'une courbe
La notion de tangente à une courbe dans l'espace est la même qu'un tangente d'une courbe dans le plan. Il s'agit de la dérivée. 

On nomme $\vec{dr}$ le vecteur unitaire tangent à la courbe. 

#### Longueur d'une courbe
On peut trouver la longueur infinitésimale d'un élément de courbe entre deux temps intégrant la dérivée de la courbe: $$dl=|\vec{r}(t+dt)-\vec{r}(t)|=|\vec{r'(d)}|dt=|\vec{v}|dt$$

$$l=\int_A^B{dl}$$
### Intégrale de ligne d'un champ vectoriel
Lorsqu'on a un champ vectoriel $\vec{F}(x,y,z)$ et une courbe paramétrée dans l'espace $\vec{r}(t)$, on peut calculer *l'intégral du champ vectoriel le long de la courbe*.
$$\int_C{\vec{F}(x,y,z)\cdot \vec{dr}}=\int_A^B{\vec{F}(x,y,z)\cdot \vec{dr}}$$
#### Application importante: le travail de force
On peut utiliser cette intégral lorsque la force $\vec{F}$ agit sur une particule selon la trajectoire $\vec{r}(t)$ pour calculer le travail exercé par la force.