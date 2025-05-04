Lorsqu'un on veut dériver un vecteur, il faut le dériver en fonction d'un référentiel. Il est plus complexe de dériver un vecteur qu'un scalaire puisque la norme et l'orientation d'un vecteur peuvent varier. 

### Dérivée ordinaire d'un vecteur
Si on a un vecteur $\vec{v}$ exprimé dans un référentiel $A$. Alors la dérivée de $\vec{v}$ dans $A$ est donné par:
$$\frac{^Ad\vec{v}}{dt} \triangleq \frac{dv_1}{dt}\vec{a}_1+\frac{dv_2}{dt}\vec{a}_2+\frac{dv_3}{dt}\vec{a}_3$$
**Il est primordial de toujours dériver selon les vecteurs unitaires du référentiel par rapport auquel on veut connaitre la dérivée.**

### Propriété d'une dérivée ordinaire ou partielle d'un vecteur
$$\begin{align}
\frac{d(\vec{u}\cdot\vec{v})}{dt} &= \frac{^Ad\vec{u}}{dt}\cdot\vec{v} + \vec{u}\cdot\frac{^Ad\vec{v}}{dt} \\
\frac{d(\vec{u}\times\vec{v})}{dt} &= \frac{^Ad\vec{u}}{dt}\times\vec{v} + \vec{u}\times\frac{^Ad\vec{v}}{dt} \\
\frac{^Ad(s\vec{u})}{dt} & = \frac{ds}{dt}\vec{u}+s\frac{^Ad\vec{u}}{dt} \\
\frac{^Ad(\vec{u}+\vec{v}+\vec{w})}{dt} & = \frac{^Ad(\vec{u})}{dt} +\frac{^Ad(\vec{v})}{dt} + \frac{^Ad(\vec{w})}{dt}
\end{align}$$

### La règle d'or

Si on a deux référentiels qui sont aligner sur l'axe z $A$ et $B$ qui sont décaler d'un angle $\theta$ respectant la règle de la main droite. On a aussi un vecteur $\vec{r}=x(t)\hat{b_x}$. On peut dériver le vecteur selon les deux référentiels.

#### En fonction de $B$
$$\begin{align}
\vec{r}&=x\hat{b_x} \\
\frac{^Bd\vec{r}}{dt}&= \dot{x}\hat{b_x}
\end{align}
$$

#### En fonction de $A$
