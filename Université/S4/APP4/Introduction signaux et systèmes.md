## Introduction
Un signal est une quantité qui varie dans le temps et qui transporte de l'information. Un système est une composante qui prend un ou des signaux en entrée et retourne un ou des signaux en sortie.

## Système linéaire temps invariant(LTI)
Il s'agit d'un système qui est linéaire (formé d'équations linéaires) et qui ne varie pas dans le temps. C'est à dire que peu importe quand on utilise le système, il va toujours retourner le même résulta pour un ensemble d'entrées donnés. Un tel système n'existe pas dans la vrai vie. Cependant, on estime que sur un certain un interval de donnée et de temps, un système peut être *LTI*.
#### Méthode de résolution de système LTI
- Résoudre directement [l'équation différentielle du système](../../S3/APP1/Méthodes%20numériques%20pour%20la%20résolution%20d'équations%20différentielles.md)
- Utiliser l'approche par [transformé](La%20transformée%20de%20Laplace.md)
- Appliquer l'opération de [convolution](Convolution.md)

### Fonction de transfert et réponse impulsionnelle
On peut décrire un système LTI d'une manière très compact qu'on appelle sa **fonction de transfert H(s)**. Celle-ci donne une **information fréquentielle** sur le comportement du système. Elle indique le **gain** et le **déphasage** que va subir toute sinusoïde pure si elle est appliqué à l'entrée du système. La sinusoïde est la **fonction propre** d'un LTI puisque la forme de la fonction demeure inchangé par le système.

On peut aussi représenter un système LTI avec sa **réponse impulsionnelle h(t)**. Physiquement, il s'Agit de la mesure de la sortie après une impulsion forte et de très courte durée. *La résonnance d'une cloche après un coup de marteau est sa réponse impulsionnelle.* Même si **H(s) et h(t)** peuvent paraitre très différente, une contient de l'information fréquentielle et l'autre temporelle, les deux contiennent la même information. On verra plus tard qu'elles sont reliés par la [transformée de Laplace](La%20transformée%20de%20Laplace.md).

Un impulsion pur est égales à la somme de cosinus à toutes les fréquences, de phase nulle et d'amplitude constante. Autrement dit, **une impulsion contient toutes les fréquences en même temps.** 

Pour savoir qu'elle représentation choisir, il faut se fier sur l'application du système et sur l'information qu'on veut en tirer.

### Autre propriété des systèmes LTI
- **Mémoire**: quand la sortie dépend de la valeur passé du signal d'entrée ou de sortie
- **Inversibilité**: si une entrée donnée correspond à une sortie unique
- **Causalité**: SI la sortie ne dépend pas du futur de l'entrée
- **Stabilité**: Un système est stable si un signal petit et faible en entrée ne produit pas un signal divergent et de durée infinie en sortie.
### Interconnexion des systèmes
On décompose souvent des systèmes en sous-systèmes pour en faciliter l'analyse. Ces sous-sytèmes peuvent être reliés de trois principales mode d'interconnexion:
1. Série
2. Parallèle
3. Feedback
## Propriétés et manipulations des signaux
### Signaux périodiques
Un signal périodique est un signal qui possède une période fondamentale, qui se répète à l'infinie. Une représentation équivalente d'un signal périodique est son **spectre de fréquences** (ou spectre de **Fourier**). Il s'agit non pas de représenter le signal temporel lui-même mais plutôt l'énergie dans chaque fréquence présente dans le signal périodique.

##### Représentation temporelle
![temporelle](Images/Pasted%20image%2020260214140720.png)

##### Représentation fréquentielle
![frequentielle](Images/Pasted%20image%2020260214140813.png)

## Énergie et puissance
Une information importante d'une signal est son énergie et sa puissance. Une des caractéristiques d'un signal LTI est que sa réponse impulsionnelle est d'énergie finie (Elle ne diverge pas). L'énergie se calcule comme suit:
$$E=\int^{t_2}_{t_1}{|x(t)|^2dt}$$
La puissance se calcul comme suit:
$$P=\frac{1}{t_2-t_1}\int^{t_2}_{t_1}{|x(t)|^2dt}$$

