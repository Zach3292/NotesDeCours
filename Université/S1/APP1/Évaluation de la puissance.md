### Puissance moyenne statique
#### Composante simple

##### Résistance
Il faut utiliser l'équation: $$P = VI = RI^2 = \frac{V^2}{R}$$
##### Capacité et inductance
Les capacités et inductances emmagasinent de l’énergie et la redonnent au circuit. Elles dissipent de l’énergie seulement par les pertes ohmiques. **Dans notre cas, ces pertes en DC sont négligeables et nous n’allons pas en tenir compte.**
##### Composante non-linéaire
Pour les composantes non-linéaires telles que les diodes et les transistors, il faut utiliser l'équation suivante: $$P=VI$$
Par exemple, un diode ayant une perte de $0.7 \ V$ avec un courant de $1 \ A$ aura une puissance moyenne statique de $0.7 \ W$.

#### Composante complexe
Pour les composantes complexes tel que le 555, il faut utiliser la fiche technique pour déterminer sa puissance. On se fit à la tension minimale et maximale et au courant minimal et maximal pour faire une règle de trois avec la tension utilisée en pratique.
On utilise ensuite l'équation $P=VI$ pour déterminer la puissance.

### Puissance moyenne dynamique
#### Résistance, condensateur et inductance
Pour calculer la puissance moyenne dynamique, il fait estimer la puissance efficace ou RMS: $$P_{RMS} = V_{RMS} \cdot I_{RMS}$$
Les variantes: $$P = R \cdot {I_{RMS}}^2 = \frac{{V_{RMS}}^2}{R}$$
s'applique également. La difficulté apparait lorsqu'il faut calculer $V_{RMS}$ et $I_{RMS}$.

Pour calculer le $RMS$, on utilise la formule suivante: $$RMS = \sqrt{\frac{1}{T}\int_{0}^{T}{[S(t)]^2\ dt}}$$
Dans certains cas, il est possible d'utiliser des raccourcis tel qu'indiqué par le tableau ci-dessous:
![Pasted image 20240901111411](Pasted%20image%2020240901111411.png)

#### Composante complexe
La seule manière de l'obtenir est de regarder si elle est fournie dans la fiche technique par le manufacturier. Sinon, elle peut être omise lorsqu'on ne travaille pas avec des composantes à hautes fréquences.

### Puissance totale consommée d'un circuit ou sous-circuit
Il faut simplement additionner la puissance individuel de chaque composante du circuit ou sous-circuit.

### Mesure pratique de la puissance consommée
Il faut s'assurer que l'impédance des sondes ou de l'oscilloscope ne viennent pas modifié le circuit en ajoutant une résistance.

Il est possible d'ajouter une petite résistance *(1 à 30 Ohms)* en série avec le circuit et d'évaluer la tension au travers de cette résistance. On peut ensuite calculer le courant la traversant à l'aide de la [loi d'Ohm](Le%20courant%20électrique.md#6.5%20La%20loi%20d'Ohm).