### Diviseur de voltage et de courant
#### Diviseur de voltage
Lorsque des résistances sont en série, elles forment un diviseur de voltage. Le voltage au travers des pattes d'un résistance est égal au produit de ratio de sa résistance sur la résistance totale et de voltage total.
$$V_1 = \frac{R_1}{R_1+R_2+R_3}V_{total}$$
#### Diviseur de courant
Lorsque des résistances sont en parallèle, elles forment un diviseur de courant. Le courant au travers des pattes d'un résistance est égal au produit de ratio de sa résistance sur la résistance totale et de courant total.
$$I_1 = \frac{R_1}{R_1+R_2+R_3}I_{total}$$
### Fonction périodique
Par convention, on écrit les sinus comme des cosinus grâce à l'identité $$\sin{(x)} = \cos{\left(x-\frac{\pi}{2}\right)}$$


### Les diodes
#### Équation de Shockley
L'équation de Shockley relie le voltage au courant pour des petites diodes de signal.
$$i_D = I_S \left[ \exp{\left(\frac{v_D}{nV_T}\right)}-1\right]$$
$I_S$ représente le courant de saturation qui est de l'ordre de grandeur de $10^{-14}A$ à $300 K$ et qui double pour chaque augmentation de $5K$.
n représente e coefficient d'émission et prend des valeurs entre 1 et 2
$i_D$ est le courant au travers de la diode
$v_D$ est le voltage au travers de la diode
$V_T$ représente le voltage thermique qui veut $$V_T=\frac{kT}{q}$$
où $k =1.38 \times 10^{-23} J/K$, $T$ est la température en kelvin et $q = 1.602 \times 10^{-19}C$ soit la norme de la charge électrique d'un électron.

#### Diode Zener
Les diodes Zeners sont des diodes qui sont fait pour fonctionner au alentour de leur voltage limite. Elles sont souvent utilisées pour faire des régulateurs de voltage. ![[Pasted image 20240902143050.png]]
#### Technique de load lines:
![[Pasted image 20240902143222.png]]

Une bonne vidéo sur les load line: https://youtu.be/TaTGnbxIMdY  
Une bonne vidéo sur les diodes en général: https://youtu.be/l2y-w9aS98k