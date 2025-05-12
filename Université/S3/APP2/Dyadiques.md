Une *dyade* est une quantité avec une magnitude associé è deux directions. Un dyadique est une somme de dyade. Il peut y avoir des dyadiques, des triadiques et des polyadiques. On appelle ces quantités des [[tenseurs]]. 

##### Quantité
- Scalaire: quantité sans direction
- Vecteur: quantité avec une direction
- Dyade: quantité avec deux directions
	- $\vec{\vec{d}}=\vec{a}\vec{b}$
- Dyadique: somme de dyades
	- $\vec{\vec{D}}=\vec{a}\vec{b}+\vec{u}\vec{v}$
### Propriété des dyadiques
- Non commutativité:
	- $\vec{a}\vec{b}\neq\vec{b}\vec{a}$
- Distributivité
	- $\vec{a}(\vec{b}+\vec{c}+\vec{d})=\vec{a}\vec{b}+\vec{a}\vec{c}+\vec{a}\vec{d}$
- Produit scalaire gauche
	- $\vec{w}\cdot(\vec{a}\vec{b}+\vec{c}\vec{d})=(\vec{w}\cdot\vec{a})\vec{b}+(\vec{w}\cdot\vec{c})\vec{d}$
- Produit scalaire droit
	- $(\vec{a}\vec{b}+\vec{c}\vec{d})\cdot\vec{w}=\vec{a}(\vec{b}\cdot\vec{w})+\vec{c}(\vec{d}\cdot\vec{w})$
- Dyadique nul et unitaire
	- $\vec{\vec{0}}\triangleq\vec{0}\vec{0}$  $\vec{v}\cdot\vec{\vec{0}}=\vec{0}$  $\vec{v}\cdot\vec{\vec{1}}=\vec{v}$

On applique une *multiplication de vecteur* comme si c'était des scalaires normaux. Il ne s'agit pas de dot-product ni de cross-product. 

### Dyadique et matrice
On peut représenter un dyadique sous une forme matricielle. 
$$\hat{a_i}\cdot\vec{\vec{D}}\cdot\vec{a_j}=\begin{bmatrix}\vec{\vec{D}}\end{bmatrix}_{\hat{a}xyz}=\begin{bmatrix}D_{xx} &D_{xy} & D_{xz} \\ D_{yx} & D_{yy} & D_{yz} \\ D_{zx} & D_{zy} & D_{zz} \end{bmatrix}_{\hat{a}xyz}$$
### Symétrie de dyadique
Un vrai dyadique est symétrique si une des équations suivantes est vrai:
$$\vec{u}\cdot\vec{\vec{D}}\cdot\vec{v}=\vec{v}\cdot\vec{\vec{D}}\cdot\vec{u}$$
$$\vec{\vec{D}}\cdot\vec{v}=\vec{v}\cdot\vec{\vec{D}}$$
