### 5.1 La capacité d'un condensateur
Un condensateur emmagasine de l'énergie, ça permet de compenser pour les variations de tensions dans la source.

Pour charger un condensateur, il faut utiliser une source de force électromotrice aussi appelée source de tension.

La capacité d'un condensateur est la suivante:
$$C =\frac{Q}{\Delta V} \left[\frac{C^2}{J}\right]\left[\frac{C}{V}\right]\left[F\right]$$

Chaque condensateur possède une différence de potentiel maximale. Si elle est dépassée le diélectrique est ionisé et endommagé de manière permanente.
### 5.2 Types de condensateur
#### Condensateur plan: 
Soit deux plans chargés $Q$ et $-Q$ d'aire $A$ séparés d'une distance $d$ par un diélectrique avec un kappa de $K$:
$$C=\frac{KA\epsilon_0}{d}$$
#### Condensateur cylindrique
Soit un petit cylindre dans un plus grand cylindre de longueur $L$. Les deux sont séparés par une distance $l$.
$$C=\frac{2\pi\epsilon_0 LK}{\ln{\frac{b}{a}}}$$
*À faire, la preuve de ça*
#### Condensateur sphérique
Soit une sphère de rayon $a$ dans une autre sphère de rayon $b$:
$$
\begin{align}
C & = \frac{Q}{\Delta V} \\
\Delta V & = -\int{\vec{E}\cdot d\vec{s}} \\
\Delta V & = -\frac{Q}{4\pi\epsilon_0 r} \biggr\rvert^b_a \\
\Delta V & = -\left(\frac{Q}{4\pi\epsilon_0 b} - \frac{Q}{4\pi\epsilon_0 a}\right) \\
\Delta V & = -\frac{aQ - bQ}{4\pi\epsilon_0 ab} \\
C & =\frac{4\pi\epsilon_0Kab}{b-a} \\
\end{align}
$$

### 5.3 L'énergie emmagasinée dans un condensateur
L'énergie potentielle emmagasinée est décrite comme suit:
$$\Delta U = \frac{Q^2}{2C} = \frac{1}{2}Q\Delta V = \frac{1}{2}C\Delta V^2$$
#### Densité d'énergie
La densité d'énergie $u$ emmagasinée se calcule comme suit:
$$\begin{align}
U & = \frac{1}{2}C\Delta V^2 \\
  & = \frac{1}{2}\left(\frac{\epsilon_0A}{d}\right)\left(Ed\right)^2 \\
  & = \frac{1}{2}\epsilon_0 E^2 Ad
\end{align}$$
$$u = \frac{U}{V} = \frac{\epsilon_0}{2}E^2 \left[\frac{J}{m^3}\right]$$
### 5.4 Association des condensateurs
#### En série
$$Q_{res} = Q_1 = Q_2 = Q_3 $$
$$\Delta V_{res} = \Delta V_1 + \Delta V_2 + \Delta V_3$$
$$\frac{Q_{res}}{C_{res}} = \frac{Q_1}{C_1} + \frac{Q_2}{C_2} + \frac{Q_3}{C_3}$$
$$\frac{1}{C_{res}} = \frac{1}{C_1} + \frac{1}{C_2} + \frac{1}{C_3}$$
#### En parallèle
$$Q_{res} = Q_1 + Q_2 + Q_3$$
$$\Delta V_{res} = \Delta V_1 = \Delta V_2 = \Delta V_3$$
$$C_{res}\Delta V_{res} = C_1\Delta V_1 + C_2\Delta V_2 + C_3\Delta V_3$$
$$C_{res} = C_1 + C_2 + C_3$$
#### Les deux ensembles
Soit le circuit suivant:

![Pasted image 20240215155314](Pasted%20image%2020240215155314.png)
$C_3$ et $C_4$ sont en série alors:
$$C_{34} = \left(\frac{1}{C_3}+\frac{1}{C_4}\right)^{-1}$$
![Pasted image 20240215155341](Pasted%20image%2020240215155341.png)
$C_2$ et $C_{34}$ sont en parallèle alors:
$$C_{234} = C_2 + C_{34}$$
![Pasted image 20240215155408](Pasted%20image%2020240215155408.png)
$C_1$ et $C_{234}$ sont en série alors:
$$C_{1234}=\left(\frac{1}{C_1}+\frac{1}{C_{234}}\right)^{-1}$$
![Pasted image 20240215155443](Pasted%20image%2020240215155443.png)
