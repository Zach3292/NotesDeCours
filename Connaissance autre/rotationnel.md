### Résumé
Le résumé du rotationnel est expliqué ici: [](Analyse%20vectorielle.md#Rotationnel) 
Si on défini le [gradient](gradient.md) comme suit:
$$\nabla = \left[ \begin{align} & \frac{\partial }{\partial x} \\ & \frac{\partial }{\partial y}\\& \frac{\partial }{\partial z}  \end{align} \right]$$Et que nous avons une fonction vectorielle $f$:
$$\vec{f} = \left[ \begin{align} & f_1(x,y,z) \\ & f_2(x,y,z) \\ 
& f_3(x,y,z)  \end{align} \right]$$
Alors on défini le rotationnel de $f$ comme:
$$\nabla\times\vec{f}=\left[ \begin{align} & \frac{\partial}{\partial x} \\ & \frac{\partial}{\partial y} \\
& \frac{\partial}{\partial z} \\ \end{align} \right] \times \left[ \begin{split} & f_1 \\ & f_2 \\
& f_3 \\ \end{split} \right] = \begin{vmatrix} \vec{i} & \vec{j} & \vec{k} \\ 
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
f_1 & f_2 & f_3 \end{vmatrix}$$
Le rotationnel prend un champ de vecteur et retourne un champ de vecteur

Si on évalue le rotationnel d'un champ de vecteurs 2D, alors il sera toujours dans la direction perpendiculaire au 2 dimensions du champ de vecteurs. Par exemple, si la base du champ est $\vec{i}$ et $\vec{j}$, alors le rotationnel sera toujours orienté dans $\vec{k}$.

Le rotationnel d'un gradient est toujours nul$$\nabla\times\nabla f = 0$$pour tous f

La divergence d'un rotationnel est toujours nulle$$\nabla\cdot(\nabla\times\vec{f}) = 0$$pour tous $\vec{f}$

### Exemple:
$$\vec{f} = \left[ \begin{align} & f_1(x,y,z) \\ & f_2(x,y,z) \\ 
& f_3(x,y,z)  \end{align} \right] = \left[ \begin{split}  & xy \\  - & \sin{ z} \\ 
& 1  \end{split} \right]$$
$$ \nabla\times\vec{f} = \cos{x} \ \vec{i} - x \ \vec{k}$$
On peut calculer la vitesse linéaire d'un point à distance $\vec{r}$ de l'axe de rotation dans un objet en rotation autour d'un axe représenté par un vecteur $\vec{a}$ et qu'il tourne à une vitesse angulaire $\omega$: $$\vec{v} = \vec{\omega}\times\vec{r}$$ et $$\vec{\omega} = \omega \ \vec{a}$$
Alors: $$\nabla\times\vec{v} = 2\omega \vec{a}$$
Ainsi, le rotationnel du champ de vecteurs de vitesse linéaire est égal à deux fois la vitesse angulaire de cette objet autour de l'axe de rotation.
Un rotationnel constant correspond alors à un rotation d'un objet solide qui ne se déforme pas