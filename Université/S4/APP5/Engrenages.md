![](Pasted%20image%2020260310160329.png)
![](Pasted%20image%2020260310160741.png)

### Terminologie

La formule la plus simple des engrenages est:
$$\frac{\omega_p}{\omega_g}=-\frac{d_g}{d_p}$$

Il est important de se rappeler que le diamètre d'un engrenage refers toujours à son *pitch diameter*. Si on parle d'un autre diamètre, il faudra toujours le spécifié explicitement.

Si on a le *pitch $p$*, et le nombre de dent $N$ on peut trouver le diamètre:
$$p=\frac{\pi d}{N}$$
![](Pasted%20image%2020260310161058.png)

Plus utilisé est le *diametrical pitch* (utilisé seulement avec les unités anglaises) et le *module* (utilisé seulement avec le SI).
$$P=\frac{N}{d}$$
$P$ en dents/pouces
$$m=\frac{d}{N}$$
$m$ en mm/dents

Le standard pour l'*addendum* est de $m$ et pour le *dedendum* $1.25m$. L'angle de pression le plus commun est $20\degree$.

Lorsqu'on a un engrenage interne, le diamètre est négatif par convention.
![](Pasted%20image%2020260310161714.png)
### Interférence
![](Pasted%20image%2020260310162406.png)

Pour calculer l'interférence, il faut calculer le rayon de l'addendum:
$$r_a=r+a$$
On peut aussi trouver le rayon d'addendum maximal sans interférence avec:
$$r_{a_{max}}=\sqrt{r_b^2+c^2\sin^2{\phi}}$$
Où $r_b$ est le rayon du cercle de base, $c$ est la distance centre-centre et $\phi$ est l'angle de pression.

On peut calculer le ratio de contact $CR$ de deux engrenages avec la formule suivante:
$$CR=\frac{\sqrt{r_{ap}^2-r_{bp}^2}+\sqrt{r_{ag}^2-r_{bg}^2}-c\sin{\phi}}{p_b}$$
Où $p_b$ est défini comme suit:
$$p_b=\frac{\pi d_b}{N}$$
Où $N$ est le nombre de dent et $d_b$ est le diamètre du cercle de base:
$$d_b=d\cos{\phi}$$
$$r_b=r\cos{\phi}$$
$$p_b=