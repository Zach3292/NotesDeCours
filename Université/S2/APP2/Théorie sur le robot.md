### Introduction
#### LR Mate0 200iD
Il s'agit d'un bras à 6 joints ressemblant au bras humain. Il possède 6 degrés de liberté, translation en x, y, z et rotation autour de x(Yaw), y(Pitch), z(Roll). On peut combiner ses rotations pour obtenir un rotation finale totale. 
#### Simulation
La simulation permet de créer des programmes hors-lignes et de définir des repères qui seront utilisés par les programmes. Pour faire une bonne simulation, il faut que l'environnement soit réaliste. Ça permet de valider que:
- le robot ne génèrent pas de contact avec d'autres éléments
- le robot reste à l'intérieur de l'environnement de travail *(ensemble des positions physiques où le robot peut se rendre)*
- le robot ne génèrent pas de changement de configuration trop rapide entre deux positions.

#### Bon à savoir
On parle parfois d'*enseigner* un parcours au robot avec une liste de points. On peut faire bouger le robot de façon manuelle en utilisant la manette *(teach pendant)* pour l'amener à des points précis *(jog the robot)*.

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
Le repère world (0,0,0,0,0,0) est situé sur le 2e joint du robot, à 330mm de la base. Il est aussi appelé *Uframe0*. Il s'agit du repère principal, les ob