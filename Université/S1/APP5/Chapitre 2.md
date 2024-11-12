### 2.1 Résistance en série et parallèle
Voir [](Circuit%20à%20courant%20continu.md#7.4%20Associativité%20des%20résistances) pour les formules
### 2.4 Analyse de voltage avec la méthode des noeuds
Nécessaire lorsque [](Circuit%20à%20courant%20continu.md#7.2%20Les%20lois%20de%20Kirchoff|les%20loi%20de%20Kirchhoff) ne peuvent pas être utilisé ni les principes de diviseur de tension et de courant.
#### Sélection du point de référence
En théorie, on peut choisir n'importe quelle noeud comme référence mais choisir un des noeuds de la source de voltage est recommandé puisque cela simplifie les calculs. 
#### Assignation des voltages de point
Pour chaque noued qu'on veut évaluer, il faut lui assigné un voltage $v_x$ qui représente la différence de tension entre ce noeud et la référence. 

#### Équation
Ensuite, on calcule le voltage de chaque composante en fonction de nos noeuds choisis plus tôt. Quand on a trouver toute les équations, on les écrit de la manière standard. On place les termes incluant les voltages de noeuds à gauche de l'équation et les autres termes à droites. 
#### Résoudre
On place ensuite les équation dans une matrice et on fait une résolution de système d'équation linéaire ([](Résolution%20de%20systèmes%20d'équations%20linéaires.md#Méthode%20de%20Gauss%20Jordan|Gauss-Jordan) ou [](Résolution%20de%20systèmes%20d'équations%20linéaires.md#Règle%20de%20Cramer|Cramer)). 

##### Avec source de tension indépendante
S'il y a plusieurs source de tension dans le circuit, on peut faire des *supernoeuds* autour des sources de tension et des points associés. On peut calculer le courant sortant de ce *supernoeuds* et il sera toujours égal à zéro selon les lois de Kirchhoff. 

#### Résumé de la méthode
1. Combiner les résistances en parallèle et en série et assigner les noeuds de référence.
2. Écrire les équations de noeuds et des *supernoeuds* en commençant par [](Circuit%20à%20courant%20continu.md#Loi%20des%20noeuds|KCL) et ensuite [](Circuit%20à%20courant%20continu.md#Loi%20des%20mailles|KVL) si nécessaire.
3. Substituer les variables controlantes des sources dépendantes par leur valeur.
4. Mettre les équations en forme standard et résoudre le système pour trouver les tensions aux points.
5. Utilisé les valeurs pour trouver les courants ou tensions d'intérêts.

### 2.5 Analyse de courants maillés avec la méthode des boucles
Utile pour les circuits dit *plan*, qui peuvent être mis à plat sans qu'aucune des composantes ne doivent se croiser.

On définit un courant se promenant dans le sens horaire pour chaque boucle du circuit.
![Pasted image 20241103142045](Pasted%20image%2020241103142045.png)
Quand plusieurs maille de courant circulent au travers d'une même composante, on considère que le courant de la composante vaut la somme algébrique de chaque maille. *Dans l'image ci-dessus, le courant de $R_2$ vaut $i_3-i_1$.* 

#### Écrire les équations
Pour écrire les équations permettant de résoudre les circuits à courant maillé, on fait simplement KVL en suivant chaque maille, pas besoin d'utiliser KCL. **Cela est valide s'il y a uniquement des résistances et des sources indépendantes.** On additionne les résistances de chaque maille et elles sont égales à la source de cette maille.

#### Circuits maillés avec source de courant
S'il y a une source de courant, on n'évite de faire KVL pour cette maille puisqu'on ne connait pas la tension au travers de la source de courant. **Ce n'est pas zéro!**

##### Source dans une seule maille
Si la source de courant est dans une seul maille, on peut simplement remplacer la valeur de courant inconnu de la maille par le courant de la source. 

##### Source dans plusieurs mailles
Si la source est dans plusieurs mailles, on défini une *supermaille* autour des mailles contenant la source et on l'évalue comme une maille standard.

#### Circuit maillé avec source dépendante
On fait simplement remplacer la variable controlante par sa valeur et procède comme habituellement.

### 2.6 Équivalence Thévenin et Norton
![Pasted image 20241103185510](Pasted%20image%2020241103185510.png)
Bonne vidéo youtube sur les équivalences: https://youtu.be/-kkvqr1wSwA?si=dGCnqdKgt_sbQnFt
Autre bonne vidéo avec une autre méthode lorsqu'il y a des sources dépendantes: (Anglais incompréhensible) https://youtu.be/i_VtXMLFmOs?si=0tRxZrv95n3PmHnq
#### Équivalence Thénevin
Représente une source indépendante de tension et un résistance en série.

Le voltage Thévenin est égal au voltage du circuit ouvert du réseau original.

La résistance Thévenin est égale au voltage du circuit ouvert divisé par le courant de court-circuit du réseau original. $$R_{th}=\frac{V_{co}}{I_{cc}}$$

S'il n'y a aucune source dépendante, on peut trouver la résistance Thévenin en *zéroant* les sources, on remplace les sources de tensions par des court-circuits et les sources de courant par des circuits ouverts. On calcule ensuite la résistance équivalente entre les deux bornes.

##### Thévenin avec source dépendante
On ne peut pas utiliser le raccourci pour la résistance alors on doit calculer à la main

*Pour trouver la résistance, on peut ajouter une source de tension de $1V$ entre les points A et B et calculer le courant entre ces points pour calculer la résistance avec la loi d'Ohm ou ajouter une source de courant indépendante de $1A$  et calculer la tension entre ses points pour calculer la résistance avec la loi d'Ohm.*

#### Équivalence Norton
Consiste à une source de courant en parallèle avec une résistance.

Cette résistance est égal à la résistance de Thévenin.

Le courant Norton est égal au courant de court-circuit. On peut utiliser l'équivalent Norton avec la même méthode que pour l'équivalent Thénevin.

#### Transformation de source
Il est possible de remplacer une source de tension en série avec un résistance par un équivalent Norton, on appelle ça faire une transformation de source. De l'extérieur, les deux circuits sont équivalent, par contre, le courant dans la résistance n'est pas le même dans les deux cas.

Il est parfois utile de faire une transformation de source pour résoudre un circuit.

#### Maximisation de puissance
Si on veut trouver la résistance qui maximiser la puissance au travers de celle-ci, on remplace par l'équivalent Thévenin et la résistance qui maximisera la puissance est égale à la résistance de Thévenin.

### 2.7 Principe de superposition
Dans un circuit avec des sources dépendantes, des résistances et $n$ source indépendantes, le courant passant au travers d'une composante ou le voltage à ses bornes s'appelle la réponse. 

Selon le principe de superposition, si on calcule la réponse du circuit avec seulement 1 source indépendantes d'active, ensuite avec 2 etc jusqu'à $n$, on va obtenir la réponse pour chaque possibilité. La réponse totale du circuit est la somme de toutes les réponses individuelles. **Le principe fonctionne juste dans un circuit linéaire.** 

Utiliser le principe de superposition permet de simplifier les calculs de composantes du circuit.

### 2.8 Pont Wheatstone
Le pont wheatstone utile pour trouver la valeur d'une résistance inconnue. 
![Pasted image 20241103154409](Pasted%20image%2020241103154409.png)
Le courant au détecteur est nul lorsqu'il est balancé.