On représente une droite par le symbole $\Delta$. Il y a plusieurs formes d'équations possible

### Forme d'équation de droite
#### Équations standards
$$\Delta: y=mx+b$$
#### Équations avec l'inclinaison
$$\Delta:y=x\tan{\theta} + b$$
#### Équations vectorielles
$\vec{d}$: Vecteur directeur de la droite
$p$: Point connu de la droite
$k\in\mathbb{R}$ 
$$\Delta: \begin{bmatrix} x & y \end{bmatrix}= \begin{bmatrix} p_1 & p_2 \end{bmatrix} + k\begin{bmatrix} d_1 & d_2\end{bmatrix}$$
#### Équation paramétriques
$k\in\mathbb{R}$ 
$\vec{d}$: Vecteur directeur de la droite
$p$: Point connu de la droite
$$\Delta:\left\{\begin{array}{l} x = p_1 +kd_1 \\ y = p_2 +kd_2\end{array}\right.$$
$$m=\frac{d_2}{d_1}$$
#### Équations symétriques
$$\Delta:\frac{x-p_1}{d_1}=\frac{y-p_2}{d_2}$$
Si $d_1,d_2\neq0$ 
#### Équations cartésiennes
$\vec{n}$: Vecteur normal à la droite
$\vec{n}=\begin{bmatrix}a & b\end{bmatrix}$ 
$$\Delta:ax+by=c$$
$$c=ap_1+bp_2$$
### Position relative de deux droites
Distinctes: $\vec{d_1}\parallel\vec{d_2}$ aucune intersection
Confondues: $\vec{d_1}\parallel\vec{d_2}$ infini intersection
Concourantes: $\vec{d_1}\nparallel\vec{d_2}$ une intersection
#### Distance d'une droite à un point $Q$
$$\|\vec{QP_\vec{n}}\|=\frac{\left|\vec{QP}\cdot\vec{n}\right|}{\|\vec{n}\|}=\left|\frac{aq_1+bq_2-c}{\sqrt{a^2+b^2}}\right|$$En forme cartésienne
#### Point sur la droite $R$ le plus proche d'un point extérieur à cette droite $Q$
$$\vec{OR}=\vec{OQ}+\vec{QP_\vec{n}}$$
$$\vec{OR} = \vec{OQ}+\frac{\left(\vec{QP}\cdot\vec{n}\right)}{\left(\vec{n}\cdot\vec{n}\right)}\vec{n}$$
#### Distance entre deux droites parallèles
$$\left|\frac{c_2-c_1}{\sqrt{a^2+b^2}}\right|=\left|\frac{aq_1+bq_2-c_1}{\sqrt{a^2+b^2}}\right|$$En forme cartésienne
#### Angle entre deux droites concourantes
Calculer l'angle entre les vecteurs normales ou les vecteurs directeurs avec [[Vecteurs du plan#Angle entre deux vecteurs|cette technique]], valeur entre 0 et $\pi/2$.