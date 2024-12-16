### 4.1 Circuit RC de premier ordre
La charge et la décharge d'un condensateur dans un circuit RC est dirigé par une équation différentielle. Lorsque résolu, on obtient les équations [ici](Circuit%20à%20courant%20continu.md#7.7%20Circuits%20RC) tel que vu [ici](Équations%20différentielles%20linéaires%20du%20premier%20et%20second%20ordre.md#Circuit%20RC).
### 4.2 État stable DC
Lorsqu'ils sont à l'état stable, les condensateurs agissent comme un circuit ouvert et les inducteurs comme un court-circuit. Pour résoudre un système RLC stable, il faut seulement remplacer les composants par leur équivalent et calculer.
### 4.3 Circuit RL
On fait comme pour les circuits RC, on applique les lois de Kirchhoff et on met en équation le circuit pour ensuite résoudre les équations différentielles.
### 4.4 Circuit RC et RL avec des sources générales
1. Écrire les équations et les réduire en équations différentielles
2. Utiliser la méthode vue [ici](Équations%20différentielles%20linéaires%20du%20premier%20et%20second%20ordre.md#Méthodes%20de%20résolution%20pour%20les%20équations%20à%20coefficients%20constants%20de%20premier%20ordre).
### 4.5 Circuit RLC de second ordre

En faisant la mise en équation, on va obtenir une équation différentielle de second ordre comme vu [ici](Équations%20différentielles%20linéaires%20du%20premier%20et%20second%20ordre.md#Application%20aux%20circuits%20électriques%20de%20second%20ordre). $w_0$ dans le circuit représente la fréquence angulaire de résonance naturelle en radian du circuit [résonance](résonance). Lorsqu'il y a présence d'une résistance dans le circuit, il y a de l'amortissement dans celui-ci. Le facteur d'amortissement vaut donc $\zeta =\frac{\alpha}{\omega_0}$. Un circuit peut avoir un amortissement critique, sur-critique et sous-critique:
#### Amortissement critique
Lorsque le discriminant vaut zéro ou $\zeta = 1$, il y a un amortissement critique [amortissement critique](amortissement%20critique). Il s'agit de l'amortissement minimale pour ne pas créer d'oscillation dans le circuit.
#### Amortissement sous-critique
Lorsque le discriminant est plus petit que 0 ou $\zeta<1$, il y a un amortissement sous-critique [amortissement sous-critique](amortissement%20sous-critique). Dans ce mode, le circuit va résonner selon sa fréquence de [résonance naturelle](résonance%20naturelle) ou sa [résonance amortie](résonance%20amortie). 
#### Amortissement sur-critique
Lorsque le discriminant est plus grand que 0 ou $\zeta>1$, il y a un amortissement sur-critique [amortissement sur-critique](amortissement%20sur-critique). Dans ce mode, il n'y a pas d'oscillation

#### Utilité des RLC
Les différents arrangements des circuits RLC peuvent créer différents filtres de signal tel que vu [ici](Courant%20alternatif.md#Circuits%20et%20Courant%20Alternatif) où le rôle de chaque composante est expliqué.

#### RLC en parallèle
Pour un RLC en parallèle, on utilise une démarche quasiment identique qu'en série sauf que le facteur $\alpha=\frac{1}{2RC}$ au lieu de $\alpha=\frac{R}{2L}$.