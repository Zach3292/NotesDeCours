On doit faire de la sensor fusion pour obtenir des données précises de plusieurs capteurs imprécis. Un exemple où la sensor fusion est nécessaire est lorsqu'on veut savoir l'orientation d'un objet selon le référentiel de la Terre. 

Pour ce faire, on utilise un gyroscope, un accéléromètre et un magnétomètre.

### Les capteurs
#### Gyroscope
Il nous donne des valeurs de vitesse angulaire autour de ses trois axes principales. Il comporte souvent du bruit basse fréquence qui s'additionne avec le temps quand on fait l'intégral pour obtenir des angles. Ça cause ce qui est appelé du *gyro drift*. Le gyroscope est précis sur de petits intervalles de temps

#### Accéléromètre
Il donne des valeurs d'accélération linéaire dans ses trois axes. Il comporte souvent un bruit à haute fréquence qui vient impacter le calcul des angles lorsqu'on évalue l'angle avec de la trigonométrie des axes d'accélération. L'accéléromètre donne une estimation des angles lorsqu'il est immobile.

#### Magnétomètre
Il sort des données sur l'orientation du champs magnétiques qu'il perçoit, souvent celui de la Terre s'il n'est pas proche d'un aimant.

### Méthode de sensor fusion
Pour contrer les points faibles de chaque capteur, on peut utiliser différente technique, la plus simple est de faire un filtre complémentaire
#### Filtre complémentaire
