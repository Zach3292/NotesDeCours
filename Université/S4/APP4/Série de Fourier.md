## Introduction
*Tout signal périodique peut se représenter comme une somme de sinusoïdes pures, dont les fréquences sont des multiples entiers de la fréquence fondamentale du signal*.
## Bases sur les fonctions périodiques
### Généralités
Une sinusoïde est définie par une **amplitude $A$**, une **pulsation $\omega$** en rad/s et une **phase $\phi$** en rad suivant la formule suivante:
$$x(t)=A\cos{(\omega t + \phi)}$$
La fréquence $f$ et la période $T$ de la sinusoïde sont également définies par:
$$f=\frac{\omega}{2\pi}$$$$T=\frac{1}{f}=\frac{2\pi}{\omega}$$
### Représentation polaire
Les harmoniques d'un signal sont des sinusoïdes dont les fréquences sont régulièrement espacées. Les harmoniques d'un signal de période $T$ sont de fréquence qui sont des multiples de $\frac{1}{T}$. Ainsi la somme des harmoniques ne peut donner qu'un signal qui à la même période que le signal original.

Quand on crée un signal en ajoutant des harmoniques, on appelle cette forme des séries de Fourier, la **forme polaire du spectre**. On peut observer graphiquement ces spectres:
![](Images/Pasted%20image%2020260214150053.png)
### Représentation complexe
Les exponentielles complexes sont une forme très compacte et très utile des fonctions harmoniques, On utilise alors la [formule d'Euler](Note%20de%20cours.md#Formule%20d'Euler) pour obtenir la **forme complexe du spectre**. 
$$\cos{\theta}=\left(\frac{e^{j\theta}+e^{-j\theta}}{2}\right)$$
$$A\cos{(\omega t + \phi)}=A\left(\frac{e^{j(\omega t + \phi)}+e^{-j(\omega t + \phi)}}{2}\right)=\left(\frac{A}{2}e^{j\phi}\right)e^{j\omega t}+\left(\frac{A}{2}e^{-j\phi}\right)e^{-j\omega t}$$
Puisqu'il faut deux harmoniques complexes pour faire un cosinus réel, chaque harmonique fera apparaitre 2 raies spectrales dans le spectre complexe: une à $\omega t$, l'autre à $-\omega t$.
![](Images/Pasted%20image%2020260214150854.png)On retrouve des valeurs positives et négatives de $k$. Les valeurs positives sont des exponentielles de fréquence "positive" ($e^{j\omega t}$)et les valeur négatives sont des exponentielles de valeur "négative" ($e^{-j\omega t}$). 

On interprète le spectre comme suit: le signal est formée de la somme de 8 exponentielles complexes, de fréquences $k\omega_0$ où $\omega_0$ est la pulsation fondamentale et $k$ est le numéro de l'harmonique.
### Symétrie des spectres
Les spectres ont des propriétés sur leur parité:
- Le spectre d'amplitude est pair
- Le spectre d'amplitude est impair
## Calcul des coefficients de Fourier
### Définition
Lorsqu'un signal est périodique, on dit qu'il peut s'exprimer comme une somme d'harmoniques de fonctions sinusoïdes pures. On l'exprime mathématiquement comme suit:
$$x(t) = C_0+\sum_{k=1}^\infty{C_k\cos{(k\omega_0t+\phi_k)}}$$
Où $C_0$ est la composante continue (DC), $C_k$ et $\phi_k$ sont respectivement l'amplitude et la phase de l'harmonique $k$, et $\omega_0$ est la fréquence fondamentale du signal $x(t)$. On peut aussi le réécrire avec la forme exponentielle plutôt que polaire:
$$x(t)=\sum_{k=1}^\infty{X_ke^{jk\omega t}}$$
Dans cette forme, $X_k$ sont des nombres complexes qui contiennent à la fois la phase et l'amplitude des harmoniques $k$.