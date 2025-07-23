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
Il s'agit d'une approximation à l'aide de la série de Taylor de deuxième degré. On doit donc itérer pour converger vers la vraie valeur de la racine puisqu'on omet les termes d'ordres supérieurs. On a donc la formule suivante: $$f(x_0)+f'(x_0)(x_r-x_0)=0$$
En reformulant: $$x_r=x_0-\frac{f(x_0)}{f'(x_0)}$$
La prochaine itération est donc: $$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}$$
#### Méthode de la sécante
Dans certain cas, on ne connait pas la dérivée. On peut donc estimer la valeur de la dérivée dans la formule de Newton-Raphson à l'aide de la dérivation arrière. La formule devient donc: $$x_{n+1}=x_n-\frac{x_n-x_{n-1}}{f(x_n)-f(x_{n-1})}f(x_n)$$
### Résolution de système d'équations non-linéaires
Il s'agit de la même démarche qu'avant sauf qu'on introduit une forme matricielle du problème. $$X_{n+1}=X_n-J_F^{-1}(X_n)F(X_N)$$
Où $J_F^{-1}$ est l'inverse de la [matrice jacobienne](matrice%20jacobienne) du système. Dans la vraie vie, il est parfois impossible d'obtenir les dérivées partielles composant la jacobienne. Il faut donc utilisé la méthode de la sécante pour la composer: $$\frac{\partial f_i}{\partial x_j}(X_n)\approx\frac{f_i(X_n)-f_i(X_{n-1})}{x_j^n-x_j^{n-1}}$$
