### Résumé
Le résumé de la divergence est expliqué ici: [[Analyse vectorielle#Divergence]] 
Un autre petit résumé plus complet du calcul de la divergence:$$\nabla\cdot\vec{f}=\left[ \begin{align} & \frac{\partial}{\partial x} \\ & \frac{\partial}{\partial y} \\
& \frac{\partial}{\partial z} \\ \end{align} \right] \cdot \left[ \begin{split} & f_1(x,y,z) \\ & f_2(x,y,z) \\
& f_3(x,y,z) \\ \end{split} \right] = \frac{\partial f_1(x,y,z)}{\partial x} + \frac{\partial f_2(x,y,z)}{\partial y} + \frac{\partial f_3(x,y,z)}{\partial z}$$
Dans cette démonstration, $\vec{f}$ est un *vecteur de fonction*
La divergence est un opérateur linéaire alors: $$\begin{align}\nabla\cdot(f_1 +f_2) & = \nabla \cdot f_1 + \nabla \cdot f_2 \\
\nabla\cdot (\alpha f) & = \alpha\nabla \cdot f
\end{align}$$
### Équations différentielles
La divergence peut être utiliser pour faire des équations différentielles et prédire comment un fluide va s'écouler dans un champ de vecteur:$$\vec{f}(x,y) = x\vec{i} + y\vec{j} = \left[ \begin{split} & x\\ & y \end{split} \right]$$
$$\frac{d}{dt}\left[\begin{split}& x\\ & y \end{split}\right]=\vec{f}(x,y) = \left[ \begin{split}& 1 \ \ \ 0 \\ & 0 \ \ \ 1 \end{split}\right] \left[ \begin{split} & x\\ & y \end{split} \right]$$
Si on intègre cette équation on arrive à la position du fluide au temps $t$: $$\left[\begin{split}& x\\ & y \end{split}\right](t)=\left[ \begin{split}& e^t \ x(0) \\ & e^t \ y(0) \end{split}\right]$$
### Le laplacien
Si on prend la divergence du [[gradient]] soit: $$\nabla\cdot\nabla f = \left[\begin{align} & \frac{\partial}{\partial x} \\ & \frac{\partial}{\partial y} \end{align} \right]\cdot \left[\begin{split} & \frac{\partial f}{\partial x} \\ & \frac{\partial f}{\partial y} \end{split} \right] = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2}$$
On obtient la somme des dérivées partielles secondes de $f$. On l'appelle aussi le laplacien de $f$ soit: $$\nabla^2f$$
### Exemples
#### Exemple 1:
$\vec{f}(x,y) = x\vec{i} + y\vec{j} = \left[ \begin{split} & x\\ & y \end{split} \right]$ 
Alors: $$\nabla\cdot \vec{f} = \frac{\partial x}{\partial x} + \frac{\partial y}{\partial y} = 1+1=2$$
Ce champ de vecteur a donc une divergence de 2 positive alors il diverge vers l'extérieur.

#### Exemple 2:
$\vec{f}(x,y) = -x\vec{i} - y\vec{j} = \left[ \begin{split} & -x\\ & -y \end{split} \right]$ 
Alors: $$\nabla\cdot \vec{f} = \frac{\partial (-x)}{\partial x} + \frac{\partial (-y)}{\partial y} = -1-1=-2$$
Ce champ de vecteur a donc une divergence de 2 négative alors il converge vers l'intérieur.
#### Exemple 3:
$\vec{f}(x,y) = x\vec{j} - y\vec{i} = \left[ \begin{split} - & y\\ & x \end{split} \right]$ 
Alors: $$\nabla\cdot \vec{f} = \frac{\partial (-y)}{\partial x} + \frac{\partial (x)}{\partial y} = 0+0=0$$
Ce champ de vecteur a donc une divergence nulle. Un champ de vecteur avec un divergence nulle est forcément en rotation puisqu'il ne converge et ne diverge pas.