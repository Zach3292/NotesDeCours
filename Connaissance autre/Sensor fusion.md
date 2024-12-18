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
La technique consiste à profiter des points forts de chaque capteur: le gyroscope est bon pour des petites périodes et l'accéléromètre sur de plus longue période.

Voici un diagramme de résumé: [Filtre complémentaire](Filtre%20complémentaire.canvas)

On commence par estimer les angles avec les données de l'accéléromètre en assumant qu'il est au repos *on évalue donc seulement la gravité*. On applique un filtre passe-bas pour retirer les bruit de l'accéléromètre. On multiplie ensuite ces angles par un facteur. 

Ensuite, on prend les données du gyroscope, on applique un filtre passe-bas et un très petit filtre passe-haut. On estime la vitesse de rotation autour des angles d'Euler: $$\begin{bmatrix} 
\dot{\phi} \\ 
\dot{\theta} \\ 
\dot{\psi}
\end{bmatrix}
= 
\begin{bmatrix}
1 & \sin{\phi}\tan{\theta} & \cos{\phi}\tan{\theta} \\
0 & \cos{\phi} & -\sin{\phi} \\
0 & \sin{\phi}\sec{\theta} & \cos{\phi}\sec{\theta}
\end{bmatrix} \cdot
\begin{bmatrix} 
p \\ 
q \\ 
r
\end{bmatrix}
$$
On intègre en fonction du temps pour obtenir des angles d'Euler et on multiplie par 1 moins le facteur de l'accélération. 

Ensuite, on additionne les deux estimations et on retourne la valeur estimée dans l'intégral en sommation pour continuer l'estimation du prochain instant. La méthode peut être résumé à la formule suivante: $$\hat{\phi}_{n+1}=\hat{\phi}_{ax, n}\cdot\alpha + (1-\alpha)\c