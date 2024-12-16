Système direct: respect la règle de la main de droite
Système rétrograde: inverse

**Pour la plupart des choses c'est identique aux [Vecteur de R3 et Rn](Vecteur%20de%20R3%20et%20Rn.md) sauf qu'il y a plus de dimensions**

### Produit vectoriel
Dans $\mathbb{R}^3$ seulement
$$\vec{u}\times\vec{v}= \begin{vmatrix} 
\vec{i} & \vec{j} & \vec{k} \\
u_1 & u_2 & u_3 \\
v_1 & v_2 & v_3 \end{vmatrix}$$
Le produit vectoriel donne un vecteur perpendiculaire aux deux vecteurs originaux s'ils ne sont pas nuls et parallèles.
#### Identité de Lagrange
$$\|\vec{u}\times\vec{v}\|^2=\|\vec{u}\|^2\|\vec{v}\|^2-\left(\vec{u}\cdot\vec{v}\right)^2$$
$$\|\vec{u}\times\vec{v}\|=\left(\|\vec{u}\|\|\vec{v}\|\sin{\theta}\right)$$
#### Propriétés du produit vectoriel
$$\begin{align}
\vec{u}\times\vec{v}& =-\vec{v}\times\vec{u} \\
\vec{u}\times(\vec{v}+\vec{w})& = \vec{u}\times\vec{v}+\vec{u}\times\vec{w} \\
(\vec{v}+\vec{w})\times\vec{u}& = \vec{v}\times\vec{u}+\vec{w}\times\vec{u} \\
k(\vec{u}\times\vec{v})=(k&\vec{u})\times\vec{v} = \vec{u}\times(k\vec{v}) \\
\vec{u}\times \vec{0} = &\vec{0}\times\vec{u}=\vec{0} \\
\vec{u}\times\vec{u}& =\vec{0} \\
\mathrm{Si} \ \vec{u}\times\vec{v} & = \vec{0} \rightarrow \vec{u}\parallel\vec{v}
\end{align}$$
### Produit mixte
$$u\cdot(\vec{v}\times\vec{w})= \begin{vmatrix} 
u_1 & u_2 & u_3 \\
v_1 & v_2 & v_3 \\
w_1 & w_2 & w_3 \end{vmatrix}$$
#### Propriétés du produit mixte
Si $u\cdot(\vec{v}\times\vec{w})=0$ alors les vecteurs sont coplanaires (linéairement dépendant)
$$u\cdot(\vec{v}\times\vec{w})=(\vec{u}\times\vec{v})\cdot\vec{w}$$