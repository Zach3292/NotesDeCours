### Introduction
Un signal est une quantité qui varie dans le temps et qui transporte de l'information. Un système est une composante qui prend un ou des signaux en entrée et retourne un ou des signaux en sortie.

### Système linéaire temps invariant(LTI)
Il s'agit d'un système qui est linéaire (formé d'équations linéaires) et qui ne varie pas dans le temps. C'est à dire que peu importe quand on utilise le système, il va toujours retourner le même résulta pour un ensemble d'entrées donnés. Un tel système n'existe pas dans la vrai vie. Cependant, on estime que sur un certain un interval de donnée et de temps, un système peut être *LTI*.
#### Méthode de résolution de système LTI
- Résoudre directement [l'équation différentielle du système](../../S3/APP1/Méthodes%20numériques%20pour%20la%20résolution%20d'équations%20différentielles.md)
- Utiliser l'approche par [[transformé]]
- Appliquer l'opération de [[convolution]]

### Fonction de transfert et réponse impulsionnelle
On peut décrire un système LTI d'une manière très compact qu'on appelle sa **fonction de transfert**. Celle-ci donne une **information fréquentielle** sur le comportement du système. Elle indique le **gain** et le **déphasage** que va subir toute sinusoïde pure si elle est appliqué à l'entrée du système. La sinusoïde est la **fonction propre** d'un LTI puisque la forme de la fonction demeure inchangé par le système.

On peut aussi représenter un système LTI avec sa **réponse impulsionnelle**. Physiquement, il s'Agit de la mesure de la sortie après une impulsion forte et de très courte durée. *La raisonnance d'une cloche après un coup de mart*