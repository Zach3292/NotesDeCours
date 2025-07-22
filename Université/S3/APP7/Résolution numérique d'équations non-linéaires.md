Il s'agit d'une méthode pour trouver le résultat d'équation qui non pas de solution analytique.

La méthode repose sur trois choses:
- Le point de départ $x_0$, en général, plus on part proche de la racine recherchée, plus la méthode sera efficace.
- La méthode de récurrence
- Le critère d'arrêt, la récurrence tend généralement de manière asymptotique. Il faut donc trouver un critère d'arrêt pour déterminer qu'on est assez proche du résultat.

On défini l'erreur selon une itération: $$\epsilon_n=x_n-x_r$$
Où $x_r$ est la racine théorique et $x_n$ est la valeur obtenue à l'itération $n$.

### Méthode de dichotomie (ou bissection)
On trouve les points $a_1$ et $b_1$ qui sont de chaque côté de la racine recherchée. Cela vet donc dire que $f(a_1)$ et $f(b_1)$ sont de signes opposés. Avec ces points, on trouve le point $c=\frac{a_n+b_n}{2}$ et on l'utilise pour trouver la prochaine itération:
Si $$f(a_n)f(c)>0$$
Alors
$$a_{n+1}=c$$$$b_{n+1}=b_n$$
Sinon$$a_{n+1}=a_n$$$$b_{n+1}=c$$
### Méthode Newton-Raphson
Il s'agit d'une approximation à l'aide de la série de Taylor de deuxième degré. On doit donc itérer pour converger vers la vraie valeur de la racine puisqu'on omet les termes d'ordres supérieurs. On a donc la formule suivante: $$f(x_a)+f'(x_a)(x_r-x_0)=0$$
En reformulant: $$x_r=x_0