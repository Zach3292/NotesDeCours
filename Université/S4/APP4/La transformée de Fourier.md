## Limite de la série de Fourier
Comme vu [ici](Série%20de%20Fourier.md), il est possible de remplacer un signal périodique par une somme d'harmoniques. Cependant, qu'arrive-t-il quand le signal original n'est pas périodique?

Si on prend une onde carrée et qu'on ajoute une zone de silence de plus en plus grande entre chaque pulsation, on se rapproche de plus en plus d'une fonction qui n'est pas périodique et qui devient une simple pulsation. 
![](Images/Pasted%20image%2020260216092959.png)Ici l'axe des fréquences représentes $k/T$ et non $k$. Si on fait tendre la période $T\rightarrow\infty$ et qu'on multiplie les coefficients de Fourier par la période $T$, on obtient **l'enveloppe spectral**, la courbe par laquelle passent tous les points des spectres précédents. Il s'agit de la définition de la **transformée de Fourier**.
![](Images/Pasted%20image%2020260216093343.png)
## Définition de la transformée de Fourier
### Expression mathématique
Lorsqu'on fait tendre $T$ vers l'infini, la pulsation fondamentale $\omega_0$ tend vers zéro, plus précisément vers un élément différentiel $d\omega$. Ainsi la pulsation discrète $k\omega_0$ devient une pulsation continue $\omega$. Si on part de la définition des [coefficients de Fourier](Série%20de%20Fourier.md#Définition) et qu'on fait tendre $T$ vers l'infini, on obtient la **transformée de Fourier** noté comme suit:
$$X(\omega) = \mathcal{F}\left(x(t)\right)=\int^{+\infty}_{-\infty}{x(t)e^{-j\omega t}dt}$$

De la même manière, il est possible d'écrire l'équation de synthèse de la **transformée de Fourier inverse** de $X(\omega)$. On note celle-ci comme suit:
$$x(t)=\mathcal{F}\left(X(\omega)\right)=\frac{1}{2\pi}\int^{+\infty}_{-\infty}{X(\omega)e^{j\omega t}d\omega}$$
### Comparaison avec la série de Fourier
![](Images/Pasted%20image%2020260216094408.png)
## Relation temps-fréquences
### L'impulsion de Dirac
L'impulsion de Dirac noté $\delta(t)$ est une fonction importante en analyse de signal à temps continu. Il s'agit d'une impulsion théorique d'amplitude infinie au temps $t=0$ et une amplitude nulle pour tous les autres valeurs de $t$. Cependant, son intégral vaut 1. On l'exprime comme suit:
$$\delta(t)=0 \textrm{ pour }t\neq0$$
$$\int^{+\infty}_{-\infty}{\delta(t)dt}=1$$
Une des propriétés importantes de l'impulsion de Dirac est que sa transformée de Fourier est constante et égale à 1 sur tout le spectre:
$$\mathcal{F}(\delta(t))=1$$
### Relation temps-fréquences
L'analyse de l'impulsion de Dirac nous permet d'obtenir une propriété importante de la transformée de Fourier: **Plus un signal $x(t)$ est localisé dans le temps, plus son spectre de Fourier est étalé en fréquences, et vice-versa**. 

Les deux limites sont les suivantes:
- Une composante continue (DC): le signal est complètement étalé dans le temps mais complètement localisé en fréquence à $f=0 Hz$.
- L'impulsion de Dirac: le signal est complètement localisé en temps mais complètement étalé en fréquence.
![](Images/Pasted%20image%2020260216095654.png)

Un règle de base pour estimer le spectre de Fourier d'une fonction rectangulaire est que **le lobe principal du spectre s'étend de 0 à 1/D Hz, où D est la durée du signal**.
## Transformée de Fourier de fonctions périodiques
La transformée de Fourier fonctionne aussi pour des fonctions périodiques, il faut cependant faire un analyse un peu différente des séries de Fourier. Dans les séries, il s'agit de fréquences discrètes qui représentent le signal périodique. Avec la transformée de Fourier, il s'agit plus tôt de plusieurs fréquences, il faut alors analyser les raies spectrales sur le graphique du spectre:
![](Images/Pasted%20image%2020260216100912.png)
## Propriétés de la transformée de Fourier
Expliquer [ici](../../../Collégial/4e%20session/Calcul%203/Note%20de%20cours.md#Existence%20et%20propriétés%20de%20la%20transformée%20de%20Fourier) avec plus de preuve.

### Linéarité
![](Images/Pasted%20image%2020260216101130.png)
### Changement d'échelle temporelle
![](Images/Pasted%20image%2020260216101147.png)
### Dualité temps-fréquences
![](Images/Pasted%20image%2020260216101258.png)
### Décalage temporel
![](Images/Pasted%20image%2020260216101318.png)
### Décalage fréquentiel
![](Images/Pasted%20image%2020260216101355.png)
### Dérivée dans le temps
![](Images/Pasted%20image%2020260216101433.png)