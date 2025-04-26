Dans certaine situation, il n'est pas possible d'appliquer les techniques analytiques vues au [chapitre 1](Rappel%20-%20calcul%20différentiel%20et%20intégral.md) pour calculer une dérivée ou un intégrale. Il faut donc faire de la dérivation et de l'intégration numérique.

### Différentiation numérique
Il y a trois manières de calculer une dérivée numérique: 
- Dérivation avant
- Dérivation arrière
- Dérivation centrée

#### Dérivation avant et arrière

La dérivation avant se base sur la formule de dérivation standard, elle dérive *à droite*. La dérivation arrière est une modification pour dérivée *à gauche*. Les deux formules sont vues [ici](../../../Collégial/4e%20session/Calcul%203/Note%20de%20cours.md#Forward%20difference) et [ici](../../../Collégial/4e%20session/Calcul%203/Note%20de%20cours.md#Backward%20difference). Dans ces formules, $h$ est le pas d'intégration, ou simplement le pas. Il remplace $dt$ dans une fonction analytique.

Pour déterminer la précision de notre dérivation, il faut trouver son erreur en approximent la vrai fonction avec les [[Séries de Taylor]]. **L'erreur est toujours proportionnelle au pas $h$.** 

#### Dérivation centrée
Pour obtenir une meilleur approximation, on peut utiliser la [dérivée centrée](../../../Collégial/4e%20session/Calcul%203/Note%20de%20cours.md#Central%20difference). Cependant, il faut connaitre le point précédent et suivante à l'endroit où l'on calcule la dérivé. *Ainsi, elle n'est pas applicable au premier et au dernier point.*

Cette formule offre une précision supérieur puisque **son erreur est proportionnelle au carré du pas $h$.**

#### Dérivée seconde
En calculant la dérivée centrale de la dérivée centrale, il est possible d'obtenir l'approximation de la dérivée seconde. Cela résulte à la formule suivante: $$f''(a) \approx \frac{f(a+h)-2f(a)+f(a-h)}{h^2}$$
#### Remarques
Dans la vraie vie, déterminer $h$ est souvent complexe, on utilise donc l'écart entre deux points comme $h$ dans la fonction.

### Intégration numérique
Il existe trois manières principale de calculer une intégrale numérique:
- Méthode des rectangles
- Méthodes des trapèzes
- Méthodes de Simpson

Les formules des trois méthodes sont expliquées dans la section [suivante](../../../Collégial/4e%20session/Calcul%203/Note%20de%20cours.md#Cours%208%20et%209). 

#### Méthode des rectangles
La méthode la plus simple mais aussi la moins précise. il s'Agit simplement de calculer la somme de Riemann pour la fonction avec les valeurs discrètes. Son erreur se calcule comme suit: $$|\epsilon_R|\leq h\frac{b-a}{2}M_R$$
Où $M_R$ est la valeur maximale de la dérivée seconde de la fonction entre les points $a$ et $b$.

#### Méthode des trapèzes
Pour la mise en application, la méthode des trapèzes a l'avantage d'être très simple puisqu'il s'agit seulement d'addition et de multiplication. Par contre, il faut faire attention à son erreur associé. Il est possible d'obtenir l'erreur maximale de la méthode des trapèzes à l'aide de la formule suivante: $$|\epsilon_T|\leq h^2\frac{b-a}{12}M_T$$
Où $M_T$ est la valeur maximale de la dérivée seconde de la fonction entre $a$ et $b$. 

#### Méthode de Simpson
La méthode de Simpson consiste à approximer des fonctions quadratiques entre chaque point et en calculer l'intégrale. Elle demande plus de calcule que la méthode des trapèzes mais elle est beaucoup plus précise.

Sur un intervalle $\Delta x$, où le point évaluée est le point $m$, le point précédent $a$ et le suivant $b$, la formule de Simpson est la suivante:
$$S_n(f) = \frac{\Delta x}{6}\left(f(a) + 4 f(m) + f(b)\right)$$
À partir de cette définition pour un seul sous intervalle, il est possible d'obtenir la formule suivante pour une somme de sous-intervalle de pas $h$.
$$S_n(f) = \frac{h}{3}\sum^{n/2}_{k=1}{\left(f(x_{2k-2}) + 4 f(x_{2k-1}) + f(x_{2k})\right)}$$

Cependant, pour que la méthode fonctionne, il faut que le nombre de point soit pair puisqu'on réduit notre précision en deux en disant qu'un point sur deux est un point milieu.
##### Erreur avec la méthode de Simpson
L'erreur avec la méthode de Simpson es beaucoup plus petite. Elle est donnée par la formule suivante: $$|\epsilon_S|\leq h^4\frac{b-a}{180}M_S$$
Où $M_S$ est la valeur maximale de la dérivée quatrième de la fonction entre le point $a$ et $b$.