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
### Type de mouvement
Il existe 3 types de mouvements robot : 

1. **Mouvement en Joints**
	1. Le robot fait bouger tous ses axes en même temps. Le plus rapide pour passer d'un point à un autre
2. **Mouvement Linéaire**
	1. Si on veut que le robot se rendre à une autre position avec une vitesse fixe et en ligne droite.
3. **Mouvement Circulaire**
	1. On peut aussi faire la même chose mais avec des cercles.

#### Terminaisons mouvement
##### CNT
La terminaison **CNT** *(continuous motion)* permet de ralentir le robot en arriver au point pour aller au prochain point. Une valeur de 0 à 100 définie la distance à laquelle le robot passe à la position de destination. On utilise CNT pour les mouvements les plus efficaces autour des objets.
![CNT](Images/CNT.png)

##### Fine
La terminaison FINE positionne le robot au point précis. Utile pour les parcours de soudure ou d’assemblage

#### En résumé:  
- un mouvement linéaire (L) donnera une trajectoire en ligne droite du TCP entre 2 points. Le mouvement angulaire de chacun des moteurs sera donc calculé en ce sens. 
    
- un mouvement joint (J) donnera une trajectoire quelconque du TCP entre 2 points, celle-ci étant tributaire du mouvement angulaire de chacun des moteurs. Ce mouvement est fait de façon à ce qu’il débute et termine en même temps pour chaque moteur. 
    
- une coordonnée exprimée en position cartésienne désigne une pose dans l’espace, elle est donc exprimé en 6 valeurs, 3 pour la position et 3 pour l’orientation. Cette pose en exprimée en fonction d’un repère. 
    
- une coordonnée exprimée en joints désigne la position angulaire de chacun des moteurs. Dans le cas d’un robot à 6 joints, elle est exprimée par 6 valeurs, une pour chaque joint. Il en résulte une certaine position de l’extrémité du robot.
### Singularités et limites de joints

Il peut arriver que votre robot soit pris en ‘singularité’.  Il s’agit en fait d’une position pour laquelle le robot a une multitude de solutions.  Pour l’instant, retenez simplement que si votre robot refuse de bouger et indique qu’il est en singularité, vous devrez revenir en mouvement en joint, bouger un peu le robot, puis réessayer le mouvement désiré en retournant en jog selon un repère.  ![singularity](Images/singularity.png)

### Configuration
Un robot peut avoir plusieurs postures différentes afin d’arriver à un même point dans l’espace. Cette posture est appelée « configuration » dans le monde de la robotique. La configuration du robot représente la valeur de ses paramètres afin de définir quelle posture a été choisie pour atteindre un point désiré. Un robot 6 axes peut amener un outil en huit configurations différentes. La configuration spécifie le placement du poignet, du coude et de l’épaule du robot.
#### Turn Counts
Si des articulations vont à moins que -180 degrés ou plus que +180 degrés, nous avons besoin de spécifier au robot le placement de ces articulations quand il se déplace à une position cartésienne.
Pour n'importe laquelle de ces articulations :
- Turn Count 0 correspond au quadrant d’angle entre + et – 180 degrés;
- Turn Count 1 correspond au quadrant d’angle entre 180 et 540 degrés;
- Turn Count 2 correspond au quadrant d’angle entre 540 et 900 degrés;
- Turn Count -1 correspond au quadrant d’angle entre -180 et -540 degrés;
- Turn Count -2 correspond au quadrant d’angle entre -540 et -900 degrés

### DCS
Le Dual Check Safety (DCS) est une fonctionnalité qui doit être obligatoirement mise en œuvre dans les systèmes robotisés de sorte que les limites physiques de l’environnement robotisé ne soient pas la seule chose qui limite le robot à sortir de sa zone de travail. 

Pour définir le DCS, il faut définir un environnement de travail, soit des frontières à l’intérieur desquelles le robot ne peut aller ou à l’extérieur desquels il ne peut aller. Il faut aussi définir une enveloppe représentant le volume occupé par le robot et ce qu’il transporte. Il faut considérer le volume maximal transporté par le robot.