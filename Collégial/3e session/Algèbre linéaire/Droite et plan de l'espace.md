### Forme d'équation
Très similaire au [chapitre 6](Droites%20du%20plan.md).
#### Équations vectorielles
$\vec{d}$: Vecteur directeur de la droite
$p$: Point connu de la droite
$k\in\mathbb{R}$ 
$$\Delta: \begin{bmatrix} x & y & z \end{bmatrix}= \begin{bmatrix} p_1 & p_2 & p_3 \end{bmatrix} + k\begin{bmatrix} d_1 & d_2 & d_3\end{bmatrix}$$
#### Équations paramétriques
$k\in\mathbb{R}$ 
$\vec{d}$: Vecteur directeur de la droite
$p$: Point connu de la droite
$$\Delta:\left\{\begin{array}{l} x = p_1 +kd_1 \\ y = p_2 +kd_2 \\ z = p_3 + kd_3\end{array}\right.$$
#### Équations symétriques
$$\Delta:\frac{x-p_1}{d_1}=\frac{y-p_2}{d_2}=\frac{z-p_3}{d_3}$$
Si $d_1,d_2,d_3\neq0$ 
### Position relative de deux droites dans l'espace
Parallèles distincte
Parallèles confondus
Concourantes: se croisent
Gauches: pas parallèles, pas concourantes

Faire un système d'équation pour trouver les intersections:
- 1 solution: concourantes
- Infini solution: parallèles confondues
- 0 solution: parallèle distincte (vecteur parallèle) ou gauche (vecteur non-parallèle)
#### Distance entre un point sur la droite $R$ et un point autre $Q$
$$\|\vec{QR}\|=\frac{\|\vec{PQ}\times\vec{d}\|}{\|\vec{d}\|}$$
$$\vec{OR} = \vec{OP}+\vec{PQ_\vec{d}}$$
#### Distance entre deux droites parallèles
$$\mathrm{Distance}=\frac{\|\vec{P_1P_2}\times\vec{d}\|}{\|\vec{d}\|}$$
## Plan dans l'espace
$\vec{n}$: vecteur normal du plan $\pi$
### Forme d'équation de plan dans l'espace
#### Équations cartésiennes
$$\pi:ax+by+cz=d=ap_1+bp_2+cp_3$$
#### Équations normales
$$\pi:\frac{ax+by+cz}{\sqrt{a^2+b^2+c^2}}=\frac{d}{\sqrt{a^2+b^2+c^2}}=\frac{ap_1+bp_2+cp_3}{\sqrt{a^2+b^2+c^2}}$$
#### Équations vectorielles
$r,s\in\mathbb{R}$
$\vec{u},\vec{v}$ linéairement indépendant
$$\pi: \begin{bmatrix} x & y & z\end{bmatrix}=\begin{bmatrix} p_1 & p_2 & p_3\end{bmatrix} + r\begin{bmatrix} u_1 & u_2 & u_3\end{bmatrix} +s\begin{bmatrix} v_1 & v_2 & v_3\end{bmatrix}$$
#### Équations paramétriques
$$\pi:\left\{\begin{array}{l} x = p_1 +ru_1+ sv_1 \\ y = p_2 +ru_2+ sv_2 \\ z = p_3 + +ru_3+ sv_3\end{array}\right.$$
### Position relative d'un plan dans l'espace
#### Distance d'un plan à un point $Q$
$$\|\vec{QP_\vec{n}}\|=\frac{|\vec{QP}\cdot\vec{n}|}{\|\vec{n}\|}=\left|\frac{aq_1+bq_2+cq_3-d}{\sqrt{a^2+b^2+c^2}}\right|$$
#### Point le plus près deux plans parallèles
$$\left|\frac{d_1-d_2}{\sqrt{a^2+b^2+c^2}}\right|$$
#### Angle entre plan et droite
Une droite peut être parallèle au plan ou avoir un point d'intersection
$$\alpha=\arccos{\frac{|\vec{d}\cdot\vec{n}|}{\|\vec{d}\|\|\vec{n}\|}}$$
#### Distance entre deux droites gauches
$\Delta_1$: une droite de vecteur directeur $\vec{d_1}$ passant par un point $p_1$.
$\Delta_2$: une droite de vecteur directeur $\vec{d_2}$ passant par un point $p_2$.
$$\vec{n}=\vec{d_1}\times\vec{d_2}$$
$$\mathrm{Distance}=\frac{|\vec{p_1p_2}\cdot\vec{n}|}{\|\vec{n}\|}$$
#### Intersection de deux ou plusieurs plans
Un plan peut être sécant, confondu ou parallèle. Il faut écrire les équations cartésiennes de chaque plan et résoudre pour x y z.

#### Intersection de deux droites
Trouver le plan ayant un vecteur normal au deux droites avec le produit vectoriel et qui passe par un point des deux droites
#### Angles entre deux plans
$$\theta=\arccos{\frac{|\vec{n_1}\cdot\vec{n_1}|}{\|\vec{n_1}\|\|\vec{n_2}\|}}$$
