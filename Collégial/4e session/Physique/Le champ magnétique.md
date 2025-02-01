### 8.1 Définition
Représenté par $\vec{B}$

Il s'agit d'une force à distance

Il y a deux théorème qui le décrivent:
1. Biot-Savart (comme  [la loi de Coulomb](La%20charge%20électrique.md#La%20force%20de%20Coulomb))
2. Le théorème d'Ampère (comme [le théorème de Gauss](Le%20théorème%20de%20Gauss.md))

### 8.2 Loi de Biot-Savart
Respecte le principe de superposition
$$\vec{B}=\frac{\mu_0i}{4\pi}\int{\frac{\vec{du_l}\times\vec{du_r}}{r^2}}$$
Où $\mu_0$ est la constante magnétique et vaut $4\pi\times 10^{-7} \ Tm/A$
### 8.3 Champ magnétique d'un fil infini
$$\vec{B}=\frac{\mu_0i}{2\pi r}(\vec{u_l}\times\vec{u_r})$$
### 8.5 Le théorème d'Ampère
Le flux magnétique est nul:
$$\Phi_B=\oint{\vec{B}\cdot\vec{dA}}=0$$
Par contre, la circulation magnétique([le curl](../../../Connaissance%20autre/Analyse%20vectorielle/Rotationnel.md)) ne l'est pas:
$$\oint{\vec{B}\cdot\vec{ds}}=\mu_0i_{inc}$$
### 8.6 Solénoïdes
Un solénoïde est composé de plusieurs boucles à courant continu. Pour avoir un solénoïde idéal, il faut respecter quelques conditions:
- Longueur >>> rayon
- Spire se touche
- Le champ magnétique à l'extérieur est nul
On défini $n=N/L$ comme étant le nombre de tours par mètre. Ainsi:
$$B=\mu_oin$$
Et si $h$ vaut la distance par rapport au centre du solénoïde:
$$B=\frac{\mu_0i}{2}\left[\frac{L-h}{\sqrt{(L-h)^2+r^2}}+\frac{h}{\sqrt{h^2+r^2}}\right]$$