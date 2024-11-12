### 13.1 Amplificateur opérationnel idéal
La moyenne des inputs s'appelle le *common-mode signal* tandis que la différence des inputs se nomme le *differential signal*. 
#### Caractéristique d'un ampli-op idéal
- Impédance d'entrée infinie
- Gain infinie pour le *differential signal*
- Aucun gain pour le *common-mode signal*
- Bandwidth infinie

Équivalent: 
![[Pasted image 20241103155413.png]]
ou A est très grand, idéalement infinie

![[Pasted image 20241103185804.png]]
### 13.2 Amplificateur inverseur
Les ampli-op sont très souvent branché avec un retour négatif. Le signal de sortie est renvoyer en entrée en opposition au signal d'entrée. Dans ce type de configuration, le signal de sortie va atteindre la valeur nécessaire pour que le signal d'entrée ait une tension et un courant nul. 
![[Pasted image 20241103184621.png]]
Si on assume un op-amp idéal, le gain est seulement déterminer par les résistances. Dans le circuit de base d'un amplificateur inverseur, le gain est donné par l'expression suivante: $$A=\frac{-R_2}{R_1}$$ avec une impédance d'entrée égale à $R_1$ et une impédance de sortie nulle.

#### Retour positif
Lors d'un branchement avec un retour positif, le signal de sortie va augmenter jusqu'à la limite que l'ampli-op peut produire. Cependant, si le signal d'entrée était négatif, le circuit ne serait pas un amplificateur puisque la sortie serait coincé à l'extrême négatif du amp-op.

### 13.3 Amplificateur non-inverseur
![[Pasted image 20241105095703.png]]
Le gain d'un ampli non-inverse sera donné par l'équation suivante: $$A = \frac{v_o}{v_{in}} = \frac{v_o}{v_o\cdot \left(\frac{R_1}{R_1+R_2}\right)} = \frac{R_1+R_2}{R_1} = 1+\frac{R_2}{R_1}$$
### Si une broche n'est pas à zéro volt
![[Pasted image 20241105153703.png]]
On doit combiner les équations de l'ampli inverseur et de l'ampli non-inverseur. Pour la broche positive, on prend celle de l'ampli non-inverseur tandis que pour la broche on prend l'équation de l'ampli inverseur: $$ v_o = v_2\left(1+\frac{R_4}{R_3}\right)-v_1\left(\frac{R_4}{R_3}\right)$$
*Prouver par superposition des inputs sur l'output*