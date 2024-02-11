### Introduction
La formule d'Euler permet de transformer n'importe quel nombre complexe en fonction sinusoïdale et en exponentiel, simplifiant ainsi plusieurs calculs. 

Pour un nombre complexe dit cartésien, $z = a +bi$ où (a, b) sont les composantes du nombre complexe dans le plan d'Argand. Il est possible de transformer ces composantes cartésiennes en composantes polaires (r, $\theta$) et d'obtenir la forme polaire d'un nombre complexe soit:$$z = r\left( \cos{\theta} + i\sin{\theta} \right) $$ où $$r = \sqrt{a^2 + b^2}$$
Et:$$\theta = \arctan{\frac{b}{a}}$$
Alors :$$z = \sqrt{a^2 + b^2}\left( \cos{\left(\arctan{\frac{b}{a}}\right)} + i\sin{\left(\arctan{\frac{b}{a}}\right)} \right) $$
### Formule d'Euler
La formule d'Euler prend un nombre complexe en forme polaire et le transforme en fonction exponentielle comme suit:$$Ae^{i\theta} = A\left(\cos{\theta} + i\sin{\theta}\right)$$
Ainsi, notre nombre complexe $z=a+bi$ peut s'écrire comme suit:$$z = \sqrt{a^2 + b^2} \cdot e^{i\arctan{\frac{b}{a}}}$$
### Exemples:
#### Identités trigonométriques
La formule d'Euler peut être utiliser pour facilement trouver des identités trigonométriques. Prenons l'exemple de $\sin{2\theta}$ et $\cos{2\theta}$. $$\begin{align} 
\sin{2\theta} & = ? \\
\cos{2\theta} & = ? \\
e^{i2\theta} & = \cos{2\theta} + i\sin{2\theta} \\
{e^{i\theta}}^2 & = \left(\cos{\theta} + i\sin{\theta}\right)^2 \\
& = \left( \cos^2{\theta}-\sin^2{\theta} \right) + i\left( 2\sin{\theta}\cos{\theta} \right) \\
\\
\sin{2\theta} & = 2\sin{\theta}\cos{\theta} \\
\cos{2\theta} & = \cos^2{\theta}-\sin^2{\theta} 
\end{align}$$
