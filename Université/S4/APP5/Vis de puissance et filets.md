## Terminologie et standard

Sur la figure suivante, on voit la définition du *pitch $p$*, *lead $L$* et du *lead angle $\lambda$*.

Le *pitch* est la distance entre deux filets, le *lead* est la distance entre le début et la fin d'une rotation complète du filet autour de la vis.
![pLlambda](Images/Pasted%20image%2020260308114119.png)

Voici différent type de filets
![filets](Images/Pasted%20image%2020260308114319.png)
Les filets ACME sont les plus vieux et les plus communs. Le ACME stub est plus facile à faire un traitement thermique. Le carré a une plus grande efficacité mais est plus dur à machiner. Le carré modifié essaye de régler ce problème. Le buttress est utilisé pour résisté à de grandes forces axiales.

## Vis de puissance
Souvent appelé actuateur linéaire ou vis de translation. Elles sont souvent utilisées pour obtenir un grand avantage mécanique, en force ou en précision.

Si on prend l'exemple suivant:
![](Images/Pasted%20image%2020260308115740.png)
On peut simplifier en disant qu'une portion de filet fait un mouvement en triangle lorsqu'il monte.
![](Images/Pasted%20image%2020260308120958.png)
Ainsi, on peut obtenir la relation suivante: $$\tan{\lambda}=\frac{L}{\pi d_m}$$
En faisant la somme des forces sur le segment, on peut obtenir un relation entre le couple appliqué sur le levier et la force axiale sur le filet:
$$T=\frac{Wd_m}{2}\frac{f\pi d_m+L\cos{\alpha_n}}{\pi d_m\cos{\alpha_n}-fL}$$

Si on ajoute un washer ou un bearing avec un coefficient de friction $f_c$ , on obtient l'équation suivante:
$$T=\frac{Wd_m}{2}\frac{f\pi d_m+L\cos{\alpha_n}}{\pi d_m\cos{\alpha_n}-fL}+\frac{Wf_cd_m}{2}$$

Si à la place on fait descendre la charge sur le jack, on a l'équation suivante:
$$T=\frac{Wd_m}{2}\frac{f\pi d_m-L\cos{\alpha_n}}{\pi d_m\cos{\alpha_n}+fL}+\frac{Wf_cd_m}{2}$$
### Angle du filet dans le plan normal
Une relation peut être établie quand on  mesure une angle dans le plan normal et axial:
$$\tan{\alpha_n}=\tan{\alpha}\cos{\lambda}$$

### Self locking and overhauling
Un vis dite *self-locking* est une vis pour laquelle il faut appliquer un couple pour descendre une charge. Une vis dite *overhauling* possède un coefficient de friction assez bas pour que la charge descende par elle même. Si on néglige la friction du collet, une vis est *self-locking* si:
$$f\geq\frac{L\cos{\alpha_n}}{\pi d_m}$$
Même si une vis peut être *self locking* dans des conditions statiques, la vibration peut permettre à la charge de bouger quand même.
### Efficacité
Pour calculer l'efficacité d'une vis de puissance, on utilise la formule suivante:
$$e=\frac{L}{\pi d_m}\frac{\pi d_m\cos{\alpha_n}-fL}{
f\pi d_m+L\cos{\alpha_n}}$$
![](Images/Pasted%20image%2020260308203753.png)

### Contact roulant
Pour augmenter l'efficacité d'une vis, on peut utiliser une *ball bearing screw*, cette vis est souvent *overhauling* en raison de sa friction très faible. 
![](Images/Pasted%20image%2020260308204129.png)
## Stress dans une vis statique
### Torsion
$$\tau=\frac{16T}{\pi d^3}$$ où $d$ est le *root diameter*.
