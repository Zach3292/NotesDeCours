### Définition
Il s'agit des mathématiques des champs de vecteurs. Comme l'écoulement d'un fluide. Les maths de champs de vecteurs sont le langages des équations de dérivées partielles.

#### Exemples de haut niveau:
Par exemple si on prend un fluide et son vecteur est $\vec{u}(\vec{x},t) = \left[ \frac{u(x,y,t)}{v(x,y,t)}\right]$. Ce champ de vecteurs est la solution d'une équation de dérivée partielle comme $\frac{\partial\vec{u}}{\partial t}=N(\vec{u}, t)$ où N est une fonction non-linéaire quelconque. Pour chaque position à chaque moment, il y a un vecteur associé. SI on ajoute une particule $X_0 = \left[\frac{x(0)}{y(0)}\right]$  à ce champ de vecteurs, il est possible d'utiliser le champ trouvé en résolvant les équations différentielles pour prédire la position dans le futur de la particule en disant que $\frac{d}{dt}X_0 = \vec{u}({\vec{x},t})$. La position est alors $X(t) = \left[\frac{x(t)}{y(t)}\right]$.

Un autre exemple est une plaque qui est chauffé en un point avec une torche. La température $T$ peut alors être décrite comme un champ de vecteur $T(x,y,t)$ qui lui est la solution de cette équation différentielle partielle: $$\begin{align}\frac{\partial T}{\partial t} & = \alpha^2 \ \nabla^2 \ T \\ 
& = \alpha^2\left(\frac{\partial^2 T}{\partial x^2}+\frac{\partial^2T}{\partial y^2}\right)
\end{align}$$
### Résumés des différents opérateurs
#### Gradient
Le [Gradient](Gradient.md) est un vecteur de dérivées partielles soit un taux de variation selon une certaine position d'où l'équation précédente:$$\begin{align}\frac{\partial T}{\partial t} & = \alpha^2 \ \nabla^2 \ T \\ 
& = \alpha^2\left(\frac{\partial^2 T}{\partial x^2}+\frac{\partial^2T}{\partial y^2}\right)
\end{align}$$Celui permet de transformer un champ scalaire en champ vectoriel. Le vecteur du [Gradient](Gradient.md) pointe vers la plus grande variation et sa norme est la variation en elle même, soit la dérivée partielle. Voici un exemple de notation si une fonction $f(x,y,z)$ dans $\mathbb{R}^3$ est différentiable alors:$$\nabla f = \left[ \begin{align} & \frac{\partial f}{\partial x} \\ & \frac{\partial f}{\partial y} \\
& \frac{\partial f}{\partial z} \\ \end{align} \right]$$
Ou plus généralement $\nabla = \vec{i} \frac{\partial}{\partial x} + \vec{j} \frac{\partial}{\partial y} + \vec{k} \frac{\partial}{\partial z}$ 
#### Divergence:
La [Divergence](Divergence.md) est le produit scalaire du [Gradient](Gradient.md), elle prend un vecteur et retourne un scalaire. Selon cette logique, si $\vec{f}$ est un vecteur de $\mathbb{R}^3$ dans un champ de vecteur, alors:$$\nabla\cdot\vec{f}=\left[ \begin{align} & \frac{\partial}{\partial x} \\ & \frac{\partial}{\partial y} \\
& \frac{\partial}{\partial z} \\ \end{align} \right] \cdot \left[ \begin{split} & f_1 \\ & f_2 \\
& f_3 \\ \end{split} \right] = \frac{\partial f_1}{\partial x} + \frac{\partial f_2}{\partial y} + \frac{\partial f_3}{\partial z}$$ 
Elle exprime la tendance qu'un champ de vecteur diverge autour d'un certain point un peu comme un soleil ou inversement converge comme un trou. Une charge ponctuelle est un exemple de [Divergence](Divergence.md) dans le champ de vecteurs du champ électrique. Elle est positive si les champs diverge vers l'extérieur et négative s'il converge vers l'intérieur, comme une charge ponctuelle.


#### Rotationnel:
Le [Rotationnel](Rotationnel.md), "curl" en anglais, est le produit vectoriel du [Gradient](Gradient.md). Il transforme un vecteur en champ vectoriel. Si on a le même vecteur $\vec{f}$ alors:$$\nabla\times\vec{f}=\left[ \begin{align} & \frac{\partial}{\partial x} \\ & \frac{\partial}{\partial y} \\
& \frac{\partial}{\partial z} \\ \end{align} \right] \times \left[ \begin{split} & f_1 \\ & f_2 \\
& f_3 \\ \end{split} \right] = \begin{vmatrix} \vec{i} & \vec{j} & \vec{k} \\ 
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
f_1 & f_2 & f_3 \end{vmatrix}$$

Il exprime la tendance qu'on des vecteurs dans un champ à tourner autour d'un point, un [Rotationnel](Rotationnel.md) positive implique une rotation anti-horaire tandis que négatif une rotation horaire, un [Rotationnel](Rotationnel.md) nul indique une absence de rotation dans le champ de vecteur.

 
