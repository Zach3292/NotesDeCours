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

Les formules des trois méthodes sont expliquées dans la section[[../../../Collégial/4e session/Calcul 3/Note de cours.md#|Note de cours]]

