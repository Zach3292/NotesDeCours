### Définition
Il s'agit d'une manière d'obtenir une structure de donnée qui peut être cherché en $O(1)$. Cette structure s'appelle une *table de hash*. Cette structure comporte plusieurs cases qui ont chacune un index commençant à zéro. Pour choisir dans quelle case un item va être stocké, il faut utiliser une *fonction de hashing*. Cette function prend en entrée l'item qu'on veut stocker et retourne un numéro de case. Lorsqu'on cherche pour un item, on utilise la fonction de hashing et on obtient la case où est supposé être l'item. Ainsi, la recherche d'élément se fait en $O(1)$ puisqu'elle ne dépend pas de la taille de la table. 

#### Collision
Si la table est trop petite ou si la fonction de hashing n'est pas bonne, plusieurs items pourraient se retrouver dans la même case. Ce phénomène s'appelle une collision ou un *clash*. Il faut ainsi s'occuper de ce problème.

#### Facteur de remplissage
Il s'agit d'un facteur expliquant comment la table de hash est rempli. Il est calculé comme suit:
$$\lambda = \frac{\textrm{nombre d'item}}{\textrm{nombre de  case}}$$

### Fonction de hashing
Un fonction de hashing qui classe chaque item dans des cases différentes se dit *parfaite*. Si on connait les items et que la collections ne change jamais, il est possible de faire une fonction de hashing parfaite. Cependant, il est impossible de s'assurer que notre fonction de hashing est parfaite si on ne connait pas les items d'avance. 

On pourrait dire qu'une manière d'avoir une fonction parfaite serait d'avoir une case par item possible. Cette méthode fonctionne lorsqu'il n'y a pas beaucoup de possibilité mais elle devient rapidement impossible en raison de la quantité de mémoire nécessaire lorsqu'on stocke des items avec beaucoup de valeurs possibles. 

Le but est de créer une fonction de hashing qui minimise les risques de collision, est facile à calculer et distribue les items de manière égale entre les cases. Il existe plusieurs possibilités.


#### Méthode du repliement
Il s'agit de diviser l'item en parties égales, de les additionner et de prendre le modulo avec le nombre de case dans notre table. Par exemple, le numéro de téléphone 555-555-5555 deviendrait $55+55+55+55+55=275\%10=5$. Ainsi, pour une table de hash avec 10 case, le numéro serait stocké dans la case 5.
#### Méthode des carrés-milieux
Cette méthode consiste à élever au carré notre item, prendre les deux caractères du milieu et ensuite garder le modulo du résultat avec le nombre de case. On obtient ainsi un numéro de case pour l'item.

Il existe plusieurs méthodes différentes, l'important est que la méthode demeure efficace car sinon, on perd le but de la table de hash qui est d'être rapide.

### Résolution des collisions
Il existe plusieurs solutions différentes pour régler le problème des collisions, mais elles ont toute un point en comment, elles augmentent la complexité de la structure de donnée.