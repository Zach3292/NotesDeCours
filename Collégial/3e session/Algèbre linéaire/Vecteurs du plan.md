Un vecteur possède une grandeur et une orientation
**Droite de support**: droite sur laquelle repose un vecteur
**Vecteur nul**: $\vec{0}$
**Norme de $\vec{v}$**: $\| \vec{v} \|$
Deux vecteurs sont égaux s'ils ont la même dimension et orientation
Addition de vecteur: on les raboute
Lois des cosinus: $c^2+a^2+b^2 -2ab\cos{\gamma}$ 
Lois des sinus: $\frac{\sin{\alpha}}{a}=\frac{\sin{\beta}}{b}=\frac{\sin{\gamma}}{c}$

#### Relation de Chaste
$\vec{AB} + \vec{BC} = \vec{AC}$

Deux vecteurs sont parallèles si et seulement si $\vec{v}=k\vec{u}$ et $\vec{u}=k\vec{v}$ 
### Principe de base
Des vecteurs sont linéairement indépendants si et seulement si $k_1\vec{v_1}+k_2\vec{v_2}+k_n\vec{v_n}=\vec{0}$ est vrai seulement quand $k_n \neq 0$.

Le vecteur $\vec{w}$ peut être représenté en combinaison linéaire de n'importe quels $n$ vecteurs de $n$ dimensions linéairement indépendants $n$ étant la dimensions de $\vec{w}$.

#### Produit scalaire
$\vec{u} \cdot \vec{v}$
Propriétés:
- $\vec{u} \cdot \vec{v}$ = $\vec{v} \cdot \vec{u}$
- $\vec{u} (\vec{v} +\vec{w}) = \vec{u} \cdot \vec{v} + \vec{u} \cdot \vec{w}$
- $a(\vec{u} \cdot \vec{v})=(a\vec{u})\cdot\vec{v}=\vec{u} \cdot(a\vec{v})$
- $\vec{u} \cdot \vec{u} = \|\vec{u}\|^2$
- $\vec{u} \cdot \vec{v}=0 \rightarrow$ vecteurs orthogonaux

#### Espace vectorielle
$V$ est un espace vectorielle et $\vec{v_1}$, $\vec{v_2}$, $\vec{v_n}$ des vecteurs dans $V$, l'ensemble $\left\{ \vec{v_1},\vec{v_2},\vec{v_n}\right\}$ est un système générateur si tout vecteur  $\vec{u} \in V$ peut être représenté par une combinaison linéaire de l'ensemble
#### Base
Un ensemble est une base s'il est un système générateur et qu'il est linéairement indépendant
##### Orthogonale
Une base est orthogonale si chaque vecteur de cette base est orthogonale aux deux autres
##### Orthonormée
Si tous les vecteurs de la base orthogonale sont unitaires la base est orthonormée.

Pour $n$ dimensions un système ayant plus de $n$ vecteurs est obligatoirement linéairement dépendant, ça l'implique qu'une base d'espace de $n$ dimensions comporte $n$ vecteurs.

**Barycentre**: point $P$ dans un ensemble de point tel que $\vec{PP_1} + \vec{PP_2} + \vec{PP_n} = \vec{0}$ 
- Un peu comme le centre de masse

### Vecteur algébrique du plan
Représenté sous forme de matrice ou de combinaison linéaire de la base orthonormée $\vec{i}$ et $\vec{j}$.

$\|\vec{u}\| = \sqrt{u_1^2+u_2^2}$
$\theta=\arctan{\frac{u_2}{u_1}}$

Pour savoir si deux vecteurs sont un système générateur, on doit faire: $$a\vec{u}+b\vec{v}=\begin{bmatrix} x & y \end{bmatrix}$$si une valeur de $x$ et $y$ existe pour lequel le système n'admet pas de solution, il ne s'agit pas d'un système générateur.
### Changement de base

Pour faire un changement de base, on utilise la matrice de passage $P$. Soit $\vec{a}$ un vecteurs de la base $B$ qu'on veut représenté dans la base $B'$ formé de l'ensemble $\left\{\vec{u}, \vec{v}\right\}$. La matrice de passage $P$ de la base $B$ à la base $B'$ comporte les vecteurs $\vec{u}$ et $\vec{v}$ exprimés dans la base $B$ en colonne. $$P=\begin{bmatrix} u_1 & v_1 \\ u_2 & v_2 \end{bmatrix}$$
On résout $[P|\vec{a}]$ avec [[Résolution de systèmes d'équations linéaires#Méthode de Gauss Jordan|Gauss-Jordan]] pour obtenir $\begin{bmatrix} a_1 & a_2 \end{bmatrix}_{\left\{\vec{u}, \vec{v}\right\}}$ soit le vecteur $\vec{a}$ exprimé dans la base $B'$.

#### Produit scalaire algébrique
$$\vec{u}\cdot\vec{v}=\sum^n_{k=1}{u_kv_k}$$
#### Angle entre deux vecteurs
$$\theta = \arccos{\left(\frac{\sum^n_{k=1}{u_kv_k}}{\|\vec{u}\|\|\vec{v}\|}\right)}$$
#### Projection orthogonale
$\vec{u}_\vec{v}$: Projection de $\vec{u}$ sur $\vec{v}$
$\vec{u}_\vec{v}$ est parallèle à $\vec{v}$
$\vec{u}-\vec{u}_\vec{v}\perp\vec{v}$ 

$$\vec{u}_\vec{v}=\left(\vec{u}\cdot\vec{v}\right)\frac{\vec{v}}{\|\vec{v}\|^2}=\frac{\vec{u}\cdot\vec{v}}{\vec{v}\cdot\vec{v}}\vec{v}$$
$$\|\vec{u}_\vec{v}\|=\frac{\left|\vec{u}\cdot\vec{v}\right|}{\|\vec{v}\|}$$

