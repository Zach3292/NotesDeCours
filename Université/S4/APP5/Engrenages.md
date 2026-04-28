![](Images/Pasted%20image%2020260310160329.png)
![](Images/Pasted%20image%2020260310160741.png)

### Terminologie

La formule la plus simple des engrenages est:
$$\frac{\omega_p}{\omega_g}=-\frac{d_g}{d_p}$$

Il est important de se rappeler que le diamètre d'un engrenage refers toujours à son *pitch diameter*. Si on parle d'un autre diamètre, il faudra toujours le spécifié explicitement.

Si on a le *pitch $p$*, et le nombre de dent $N$ on peut trouver le diamètre:
$$p=\frac{\pi d}{N}$$
![](Images/Pasted%20image%2020260310161058.png)

Plus utilisé est le *diametrical pitch* (utilisé seulement avec les unités anglaises) et le *module* (utilisé seulement avec le SI).
$$P=\frac{N}{d}$$
$P$ en dents/pouces
$$m=\frac{d}{N}$$
$m$ en mm/dents

Le standard pour l'*addendum* est de $m$ et pour le *dedendum* $1.25m$. L'angle de pression le plus commun est $20\degree$.

Lorsqu'on a un engrenage interne, le diamètre est négatif par convention.
![](Images/Pasted%20image%2020260310161714.png)
### Interférence
![](Images/Pasted%20image%2020260310162406.png)

Pour calculer l'interférence, il faut calculer le rayon de l'addendum:
$$r_a=r+a$$
On peut aussi trouver le rayon d'addendum maximal sans interférence avec:
$$r_{a_{max}}=\sqrt{r_b^2+c^2\sin^2{\phi}}$$
Où $r_b$ est le rayon du cercle de base, $c$ est la distance centre-centre et $\phi$ est l'angle de pression.

On peut calculer le ratio de contact $CR$ de deux engrenages avec la formule suivante:
$$CR=\frac{\sqrt{r_{ap}^2-r_{bp}^2}+\sqrt{r_{ag}^2-r_{bg}^2}-c\sin{\phi}}{p_b}$$
Où $p_b$ est défini comme suit:
$$p_b=\frac{\pi d_b}{N}$$
Où $N$ est le nombre de dent et $d_b$ est le diamètre du cercle de base:
$$d_b=d\cos{\phi}$$
$$r_b=r\cos{\phi}$$
$$p_b=p\cos{\phi}$$
En général, plus le ratio de contact est grand, plus les engrenages tournent de manière fluide et silencieuse.
### Analyse de force
Pour analyser les forces sur les engrenages, on utilise $V$:
$$V=\pi dn/12$$
En unité impérial
et $$V=\pi dn/60000$$ en unité métrique (d:mm et V m/s).

Le travail transmis est le suivant:
$$\dot{W}=F_tV/33000$$
En hp où $F_t$ est en livre et la vitesse en pied par minutes
$$\dot{W}=F_tV$$
En watts avec $F_t$ en newtons
![](Images/Pasted%20image%2020260310164945.png)
### Force des dents d'engrenage (Lewis)
Pour utiliser la technique de Lewis, il faut faire les hypothèses suivantes:
- La charge complète est appliquée au bout d'une seule dent
- La composante radial $F_r$ est négligeable
- La charge est distribuée de manière uniforme sur la largeur de la face au complet
- Les forces associés à la friction des dents qui glissent sont négligeables
- La concentration de stress dans le filet de la dent est négligeable.


![](Images/Pasted%20image%2020260310165958.png)
L'équation de Lewis est la suivante:
$$\sigma=\frac{F_tP}{bY}$$
En impérial et
$$\sigma=\frac{F_t}{mbY}$$ en métrique.

Pour trouver $Y$, on utilise le graphique suivant:
![](Images/Pasted%20image%2020260310170230.png)

![](Images/Pasted%20image%2020260310171123.png)

On peut calculer le ratio d'engrenage planétaire de plusieurs manières en assumant que R, S et P sont le diamètre ou le nombre de dents:
1. Analyse de force avec DCL: $$\frac{\omega_i}{\omega_o}=1+\frac{S}{R}$$
![](Images/Pasted%20image%2020260310171706.png)

## Engrenage hélicoïdale
![](Images/Pasted%20image%2020260312074103.png)

Un engrenage droit est un engrenage hélicoïdale mais avec un *angle d'hélice* ($\psi$) nul. Les valeurs d'angles d'hélice ne sont pas standard mais se situe souvent entre 15 et 30 degrés. Pour utiliser deux engrenages hélicoïdales ensemble en parallèle, il faut que les deux aient le même angle d'hélice mais de sens opposé.

Comme pour des engrenages droits, le *pitch circulaire* et l'angle de pression sont calculé dans le plan de la rotation. Cependant, on inclut des nouvelles quantité avec des engrenages hélicoïdales. On mesure ces quantités dans le plan normal aux dents.
$$p_n=p\cos{\psi}$$
$$\tan{\phi_n}=\tan{\phi}\cos{\psi}$$
Le pitch peut aussi être calculé:
$$P_n=P/\cos{\psi}$$
Ainsi que le diamètre de pitch
$$d=N/P=N/(P_n\cos{\psi})$$
Le pitch axial aussi existe:
$$p_a=p/\tan{\psi}$$
Pour calculer le stress sur des engrenages hélicoïdales, il faut trouver le nombres de dents équivalent $N_e$ et utiliser le facteur de Lewis selon ce nombre de dents comme pour des engrenages droits.
$$N_e=N/\cos^3{\psi}$$
### Analyse de force
![](Images/Pasted%20image%2020260312075330.png)

Les calculs pour $F_t$ et $F_r$ sont les mêmes que pour des dents droites, cependant, il faut ajouter $F_a$ et $F_b$:
$$F_a=F_t\tan{\psi}$$
$$F_b=F_t/\cos{\psi}$$
$$F=F_b/\cos{\phi_n}=F_t/\cos{\psi}\cos{\phi_n}$$
## Engrenage conique
### Géométrie des engrenages coniques
![](Images/Pasted%20image%2020260312074436.png)
Pour calculer des engrenages coniques, on utilise le concept du nombre de dent d'un engrenage droit imaginaire. On dit que ces engrenages ont un rayon de pitch égal au développement d'un cône:
$$N'_p=\frac{2\pi r_{bp}}{p}$$
$$N'_g=\frac{2\pi r_{bg}}{p}$$
Où $N'$ se nomme le nombre virtuel de dent. On appelle la pratique d'estimer les caractéristiques d'engrenages coniques avec des engrenages droits s'appelle *l'approximation de Tredgold*.
![](Images/Pasted%20image%2020260312080913.png)
![](Images/Pasted%20image%2020260312080815.png)
Le ratio des engrenages peut être déterminer de plusieurs façon:
$$\textrm{Gear ratio}=\frac{\omega_p}{\omega_g}=\frac{N_g}{N_p}=\frac{d_g}{d_p}=\tan{\gamma_g}=\cot{\gamma_p}$$
Où $\gamma$ est l'angle de cône
### Analyse de force
On peut voir sur l'image suivante le force tangentielle $F_t$ (torque), la force radiale $F_r$ (séparation) et la force axiale $F_a$ appliquées sur un engrenage conique:
![](Images/Pasted%20image%2020260312081610.png)

$$d_{av}=d-b\sin{\gamma}$$
$$V_{av}=\pi d_{av}n$$
$$F_t=33000\dot{W}/V_{av}$$
$$F=F_t/\cos{\phi}$$
$$F_n=F\sin{\phi}=F_t\tan{\phi}$$
$$F_a=F_n\sin{\gamma}=F_t\tan{\phi}\sin{\gamma}$$
$$F_r=F_n\cos{\gamma}=F_t\tan{\phi}\cos{\gamma}$$
Où $F_n$ est normal au cône. Pour les engrenages coniques en spirale:
$$F_a=\frac{F_t}{\cos{\psi}}(\tan{\phi_n}\sin{\gamma}\mp\sin{\psi}\cos{\gamma})$$
$$F_r=\frac{F_t}{\cos{\psi}}(\tan{\phi_n}\cos{\gamma}\pm\sin{\psi}\sin{\gamma})$$
