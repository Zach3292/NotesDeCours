
Il y a quatre grandes familles d'analyse pour des robots:
1. Cinématique
	1. Le lien entre la position des joints et la position de l'effecteur
	2. Elle peut être directe ou inverse
	3. $\underline{r}=f\left(\underline{q}\right)$
2. Cinématique différentielle
	1. Le lien entre la vitesse des joints et la vitesse de l'actuateur
	2. Elle peut être directe ou inverse, pour faire l'inverse, on doit utiliser des matrices pseudo-inverses.
	3. $\dot{\underline{r}} = J\left(\underline{q}\right)\dot{\underline{q}}$
3. Statique
	1. Le couple ou force des joints en fonction de la force appliquer par l'effecteur
	2. $\underline{\tau}=J^T(\underline{q})\underline{f}_E$
4. Dynamique
	1. Relation entre l'accélération des joints et les forces appliquées
	2. $H(\underline{q})\ddot{\underline{q}} + C(\underline{q},\dot{\underline{q}})\dot{\underline{q}}+D\dot{\underline{q}}+\underline{g}(\underline{q})=\underline{\tau}-J^T(\underline{q})\underline{f}_E$
	3. $H$ et $C$ sont des effets inertiels, $D$ des forces dissipatrices et $g$ la forces gravitationnelle
### 1.1 L'importance de l'algèbre linéaire pour la robotique
Comme les robots on souvent un grand nombre d'entrée et de sortie et sont analysé dans des systèmes avec beaucoup de coordonnées, il est primordial d'utilisé de [l'algèbre linéaire](../../../Collégial/3e%20session/Algèbre%20linéaire/Algèbre%20linéaire.md) pour résoudre ces équations. 

### 1.4 Symboles et notations

$\vec{v}$: Vecteur

$\hat{v}$: Vecteur unitaire

$\vec{r}_{A/B}$: Vecteur position du point $A$ par rapport au point $B$

$\underline{c}$: Vecteur colonne

$\underline{v}^a$: Vecteur colonne des composantes du vecteur $\vec{v}$ dans la base $a$

$\underline{v}^a_i$: Composantes du vecteur $\vec{v}$ selon le vecteur unitaire $i$ dans la base $a$

$\underline{q}$: Vecteur colonne qui regroupe $n$ scalaires représentant la configuration d'un robot à $n$ *DDL* dans l'espace des joints

$\{\hat{a}_1, \hat{a}_2, \hat{a}_3\}$: Base vectorielle $a$ définie par une ensemble de trois vecteurs unitaires orthogonaux

$\{A_O, \hat{a}_1, \hat{a}_2, \hat{a}_3\}$: Repère $A$ défini par un point $A_O$ et la base vectorielle $a$.

$^aR^b=\begin{bmatrix}\underline{b}^a_1 & \underline{b}^a_2 & \underline{b}^a_3\end{bmatrix}$: Matrice de rotation 3x3 qui représente l'orientation de la base vectorielle $b$ par rapport à la base $a$.

$^aT^B=\begin{bmatrix} ^aR^b & \underline{r}^a_{B_O/A_O} \\ 0 \ 0\ 0 & 1\end{bmatrix}$:Matrice de transformation homogène 4x4 du repère $B$ vers le repère $A$.
