Tel que vu [ici](Introduction%20signaux%20et%20systèmes.md)], un système peut être représenter comme une boite mathématique qui prend une entrée et retourne une sortie. On va maintenant s'intéresser au cas où l'entrée est dite **forcée** (imposé à une sinusoïde pure). Les concepts suivants seront valide en **régime permanent** (steady state). Par exemple, si le régime permanent est atteint après 20 secondes, la technique de la fonction de transfert harmonique est valide pour $t>20s$. 
## Le pendule amorti en régime forcé
On va prendre en compte un pendule de masse $m$ et de longueur $l$ et soumis à un couple $\Gamma(t)$ à son point de pivot. L'équation qui régis ce système est la suivante:
$$ml^2\frac{d^2\theta}{dt^2}+cl^2\frac{d\theta}{dt}+mgl\sin{\theta(t)}=\Gamma(t)$$
Cette équation peut être résolu à l'aide de [méthodes numériques](../../S3/APP1/Méthodes%20numériques%20pour%20la%20résolution%20d'équations%20différentielles.md). Cependant, il es difficile de prédire son comportment avant l'analyse numérique. 
### Linéarisation du problème
L'équation du problème n'est pas linéaire à cause du sinus, on peut faire l'approximation que les angles sont petits donc $\sin{\theta}\approx\theta$. On obtient alors:
$$ml^2\frac{d^2\theta}{dt^2}+cl^2\frac{d\theta}{dt}+mgl{\theta(t)}=\Gamma(t)$$
### Régime harmonique - Fonction de transfert
En régime permanent, le système est excité par le couple selon l'équation suivante:
$$\Gamma(t)=e^{j\omega t}$$
La sortie est aussi une sinusoïde pure complexe qu'on peut décrire comme suit:
$$\theta(t)=He^{j\omega t}$$
On peut remplacer ces deux équations dans l'équation linéarisée et isolé H pour obtenir:
$$H=\frac{1}{-\omega^2ml^2+j\omega cl^2+mgl}=\frac{1}{ml^2}\left(\frac{1}{\left(\frac{g}{l}-\omega^2\right)+j\omega\frac{c}{m}}\right)$$
On remarque que $H$ est une fonction complexe qui dépend de $\omega$, on peut donc l'écrire comme $H(j\omega)$ et on va l'appeler la **fonction de transfert harmonique** de notre système. La fonction de transfert $H(j\omega)$ représente la réponse $\theta(t)$ lorsque le système est excité par une entrée unitaire de phase nulle. On utilisera la formule suivante pour la suite:
$$H(j\omega)=\frac{1}{ml^2}\left(\frac{1}{\left(\frac{g}{l}-\omega^2\right)+j\omega\frac{c}{m}}\right)$$
### Détermination de la sortie
Comme la sortie doit être réelle, il faut décomposer $H(j\omega)$ sous sa forme polaire:
$$H(j\omega)=A(\omega)e^{j\phi(\omega)}$$
Où $A(\omega)=|H(j\omega)|$ et $\phi(\omega)=\angle H(j\omega)$. La sortie est donc proportionnel à l'entrée, mais amplifié d'un gain $A(\omega)$ et déphasée d'un angle $\phi(\omega)$.  Ainsi, la connaissance de la fonction de transfert harmonique $H(j\omega)$ permet de connaitre la sortie du système pour n'importe quelle excitation harmonique pure.

En affichant le gain et la phase en fonction de la fréquence on peut trouver de l'information intéressante:
![](Images/Pasted%20image%2020260215205157.png)

Lorsque la fréquence vaut zéro, le gain tend vers 0.1 et la phase vers zéro, on appelle ça le **gain statique**, c'est le facteur d'amplification d'une entrée constante.

Pour des fréquences en dessous de 0.5Hz, la phase est constante et nulle. Dans ce cas, il n'y a pas de déphasage entre l'entrée et la sortie. Les deux signaux sont dit **en phase**.

Autour de la fréquence de 0.5Hz, on observe un pic soudain dans la courbe de gain. On appelle ce phénomène d'amplification de la résonance et il s'agit de la **pulsation de résonnance** du système.

Au dessus de 0.5Hz, ;e gain diminue jusqu'à atteindre zéro. De plus la phase en sortie est en **opposition de phase**.

On définit la **fréquence de coupure** (ou pulsation de coupure) la fréquence pour laquelle le gain du filtre est de -3dB si le gain de la bande passante est de 0dB.

Dans un système résonant, l'écart entre les deux fréquences de coupures est appelé la **largeur de bande**. On définit également le **facteur de qualité** noté $Q$ de la manière suivante:
$$Q=\frac{\omega_r}{BW}$$
### Vérification de la validité
Il est important de validé noter approximation faite lors de la linéarisation du système.