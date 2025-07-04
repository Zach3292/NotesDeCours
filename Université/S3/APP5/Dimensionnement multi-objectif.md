### Élaboration du cahier des charges
En général, il faut inclure les éléments suivants:
- Tension
- Volume
- Poids
- Coût
- Énergie
- Puissance
- Température
- Durée de vie

Pour chaque élément, dire la valeur minimale ou maximale ainsi que les unités. 

#### Hypothèses de conception
Les hypothèses de conception servent à simplifier le choix de conception. Elles sont à faire au choix selon les priorités du système. 

On peut par exemple supposer que la tension des cellules est parfaitement balancé.

### Calcul des spécifications de conception
#### Estimation du volume
Selon le nombre de cellule, on peut faire une approximation rapide du volume de la batterie.
$$V_{sae}=n_sn_pl(D+2e)^2$$
Où
- $n_s$: nombre de cellule en série
- $n_p$: nombre de cellule en parallèle
- $l$: longueur d'une cellule
- $D$: diamètre d'une cellule
- $e$: épaisseur de la paroi des cellules

On peut réécrire l'équation:
$$n_s\leq\frac{V_{sae}}{n_pl\frac{\pi(D+2e)^2}{4}}$$
#### Estimation de la masse
$$m_{sae}=n_sn_p(m_{cell}+m_{pcm})$$
Où
- $m_{cell}$: Masse d'une cellule
- $m_{pcm}$: Masse du système de refroidissement

On peut réécrire l'équation comme suit:
$$n_s\leq\frac{m_{sae}}{n_p(m_{cell}+m_{pcm})}$$
#### Estimation du coût
$$\textrm{Coût}=n_sn_p(\textrm{Cout/cellule+refroidissement})$$
#### Estimation de la consommation et de la puissance
Le SAE doit être en mesure de fournir la puissance maximale que peut consommer le système.
#### Estimation de l'énergie embarquée
$$E=n_sn_pV_{nom}Q_{cell}$$
#### Estimation de la tension d'opération maximale
$$V_{sae}=n_sV_{cell,max}$$
#### Estimation de la puissance
$$P_{max}=n_sV_{cell,min}n_pI_{cell,spec}$$
#### Estimation du taux de décharge
$$I_{cell,spec}=Q_{cell}\cdot C_{rate}$$
Le taux de décharge est exprimé en C (pas des Coulomb). Plus il est élevé, plus le courant maximale de la batterie sera grand.

#### Estimation de la tension minimale d'opération
$$V_{sae,min}=n_s(V_{cell,min}-R_{cell}I_{cell,max})$$
#### Estimation de la puissance minimale disponible
$$P_{min}=V_{sae,min}\left(\frac{V_{cell,min}-\left(\frac{V_{sae,min}}{n_s}\right)}{R_{cell}}\right)$$
#### Température
#### Prédiction de la durée de vie
On considère la durée de vie le nombre de temps ou de cycle jusqu'à ce que la capacité maximale tombe en dessous de 80% de la capacité initiale maximale.


**On peut seulement faire le choix d'une SAE de manière éclairée en considérant tous les critères ci-dessus.**