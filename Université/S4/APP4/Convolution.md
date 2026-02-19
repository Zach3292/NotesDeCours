## Le produit de convolution
### Définition
De façon générale, [l'impulsion de Dirac](La%20transformée%20de%20Fourier.md#L'impulsion%20de%20Dirac) $\delta(t-t_0)$ est nulle partout sauf lorsque $t=t_0$. Ainsi, multiplié un fonction par cette impulsion revient à multiplié la valeur de la fonction à $t_0$ par l'impulsion:
$$x(t)\delta(t-t_0)=x(t_0)\delta(t-t_0)$$
Ainsi pour obtenir la valeur de $x(t_0)$, il suffit d'intégrer le produit de fonction sur toute l'intervalle de temps. Il s'agit d'un propriété d’échantillonnage de l'impulsion de Dirac:
$$x(t_0)=\int^{+\infty}_{-\infty}{x(t)\delta(t-t_0)dt}$$
Si on remplace la variable dans l'intégration, il est possible de réécrire comme suit:
$$x(t)=\int^{+\infty}_{-\infty}{x(\tau)\delta(t-t\tau)d\tau}$$
C'est ce qu'on appelle **l'intégral de convolution**.
### Utilisation pour la résolution de système LTI
Pourquoi ce compliqué la vie lorsqu'on connait déjà le signal $x(t)$? Si on connait la réponse impulsionnelle du système (la réaction à une seule impulsion de Dirac), le signal $x(t)$ représente alors la somme des réponses impulsionnelles décalées du système. On peut donc trouver la sortie à partir d'un intégral de convolution. Cette intégrale porte un nom particulier dans ce cas: **l'intégrale de convolution entre le signal d'entrée et la réponse impulsionnelle du système**.
$$y(t)=\int^{+\infty}_{-\infty}{x(\tau)h(t-t\tau)d\tau}$$
Cette opération est parfois réécrite comme suit:
$$y(t)=x(t)*h(t)=h(t)*x(t)$$
Où $*$ dénote le produit de convolution.
### Interprétation de la convolution
Le terme convolution vient du latin *convolvere* qui signifie "retourner". Voici dans interprétation de la convolution, la deuxième ayant un lien avec son nom latin:

La première interprétation de la convolution est que la réponse est donnée par la somme des réponses impulsionnelles décalées, chacune étant multipliée par la valeur du signal au temps $t=\tau$. 

Pour trouver la deuxième interprétation, il faut considérer $\tau$ comme la variable de temps dans l'équation. L'opération revient alors à "retourner" la fonction $h(\tau)$ pour obtenir $h(-\tau)$ et y ajouter un décalage $t$.

### Relation temps-fréquence
D'après la relation précédente, la sortie d'nu sstème LTI peut être trouvé par une [transformée de Laplace](La%20transformée%20de%20Laplace.md) ou par une convolution:
$$y(t)=h(t)*x(t)$$
$$Y(s)=H(s)X(s)$$
On peut résumer cette propriété: **Une multiplication dans un domaine revient à faire une convolution dans l'autre.**

| **Domaine temporel** | **Domaine fréquentiel** |
| -------------------- | ----------------------- |
| $x_1(t)$             | $X_1(s)$                |
| $x_1(t)*x_2(t)$      | $X_1(s)X_2(s)$          |
| $x_1(t)x_2(t)$       | $X_1(s)*X_2(s)$         |
## La convolution pour les signaux à temps discret
