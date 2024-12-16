### 7.1 Symbole
![[Pasted image 20240902153623.png]]

### 7.2 Les lois de Kirchhoff
#### Loi des noeuds
La loi des noeuds dit que le courant entrant dans un noeud doit être le même que le courant sortant
![[Pasted image 20240902153755.png]]
#### Loi des mailles
La somme des tensions dans une maille doit être de zéro
![[Pasted image 20240902153840.png]]

### 7.4 Associativité des résistances
On additionne les résistances en série et on additionne l'inverse des résistances en parallèles
Séries: $$R = R_1 + R_2 + R_3$$
Parallèles:
$$\frac{1}{R} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3}$$
### 7.7 Circuits RC
Circuit comportant une résistance et un condensateur en série

#### Décharge du condensateur
##### Charge
$$Q(t) = Q_m e^{\frac{-\tau}{RC}}$$
##### Courant
$$I(t) = I_m e^{\frac{-\tau}{RC}}$$
#### Charge du condensateur
##### Charge
$$Q(t) = Q_m \left(1-e^{\frac{-\tau}{RC}}\right)$$
##### Courant
$$I(t) = I_m e^{\frac{-\tau}{RC}}$$