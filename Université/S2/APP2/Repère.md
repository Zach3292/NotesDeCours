### Repère
Un repère sert à définir la position de quelque chose. On repert est constitué de deux choses:
- Un origine, on définit les vecteurs positions par rapport à ce points
- Une base vectorielle, un ensemble de vecteurs qui définissent l'espace, on définit les axes de rotation W, P, R autour des vecteurs de cette base

Un repère contient donc 6 informations: x, y, z, w, p, r.

Dans un Fanuc, il y a trois repère principal:
- Le **World**
- Le **User frame**
- Le **Tool frame**.
#### Repère World
Le repère world (0,0,0,0,0,0) est situé sur le 2e joint du robot, à 330mm de la base. Il est aussi appelé *Uframe0*. Il s'agit du repère principal, les objets et les autres repères sont définis par rapport à lui.
![world](Images/world.png)
#### Repère User
Il s’agit du repère par rapport auquel on décrit les positions du robot. **Les coordonnées du _User Frame_ sont elles-mêmes définies par rapport au _World_.** Ainsi, un _User Frame_ qui n’est pas initialisé est donc à (0,0,0,0,0,0), c’est-à-dire qu’il coïncide avec le _World_.

Or, il est pratique de définir des _User Frames_ à divers endroits dans la celluleAinsi, si la configuration de la cellule venait à changer, il suffira de modifier la valeur du _User Frame_ représentant le point focal, et les positions qui auront été enseignées par rapport au _User Frame_ seront encore valides tandis que celle par rapport au *World frame* devront tous être refaite.

On constate que la définition du coin de la table est beaucoup plus simple et intuitive lorsqu’elle est exprimée en fonction du repère de la table. Sans mentionner que le repère « T1 » suivra automatiquement la table si on la déplace.

D’autre part, les _User Frames_ permettent de créer des programmes beaucoup plus faciles à comprendre. Il faut donc s’assurer d’enseigner les positions en fonction d’un _User Frame_ qui permet de simplifier la compréhension. Par exemple, une trajectoire fait sur un équipement ou une pièce devrait être défini par rapport au repère de l’équipement ou de la pièce.

#### Repère Tool
Le _Tool Frame_ est le repère outil qui est défini par rapport au bout du robot (sur le joint 6). Il est constitué du Tool Center Point et de la base vectorielle (3 vecteurs) qui définit l’orientation du repère.  Typiquement, le _Tool Frame_ est défini au bout de l’outil.

Enfin, il est important de noter que bien que ce repère porte le nom de ‘repère outil’, il n’indique pas toujours la position de l’outil. En effet, plutôt que de tenir un outil, le robot pourrait tenir un préhenseur qui ira prendre des pièces: dans ce cas-ci, le _Tool Frame_ serait probablement défini au bout du préhenseur, en son point central, soit à l’endroit où il ira prendre les pièces. On l’appellerait quand même _Tool Frame_, ce qui peut porter à confusion.

#### Système d'axe des repères
Les repères suivent un système d'axe [direct](../../../Collégial/3e%20session/Algèbre%20linéaire/Vecteur%20de%20R3%20et%20Rn.md), c'est à dire qu'il respecte la règle de la main droite pour les rotations et les translations 

#### Convention de rotation
Lorsque plusieurs rotations sont exécutées, il est important de tenir compte de l'ordre dans lequel ces rotations sont exécutés. Il existe plusieurs manière de les décrire et plusieurs conventions mais les robot Fanuc utilise la convention **Euler mobile Z'Y'X'**. Ça signifie que vous commencez par appliquer la rotation autour de Z. Vous prenez ensuite ce nouveau repère temporaire (d’où la notation Z’) et y appliquez la rotation en Y, ce qui vous donnera un 2e repère temporaire. Finalement, vous effectuez la rotation autour de X à partir de ce 2e repère temporaire, ce qui vous donne la position finale.