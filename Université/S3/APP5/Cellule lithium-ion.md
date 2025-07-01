Les cellules fonctionnent selon un transfert d'ions lithium dans une matrice de carbone. Cela crée un potentiel électrique en circuit ouvert qui est proportionnel à la quantité de charge accumulée. 

### État de charge
L'état de charge d'une cellule est exprimé en %. Il représente la capacité restante d'une batterie par rapport à sa capacité maximale. Elle se calcule comme suit:
$$E.D.C=\frac{Capacity_{AH}-PDD_{AH}}{Capacity_{AH}}*100$$
Où la profondeur de décharge est exprimée comme suit en $Ah$: $$PDD_{AH}=\int_0^t{I(t)_A*dt}$$
Exemple de la tension d'une batterie en fonction de la profondeur de décharge:
![](Images/Pasted%20image%2020250701103643.png)

### Résistance interne
Plus la résistance interne d'une cellule est grande, moins elle est efficace. En effet, elle subit plus de perte de joule. Pour mesurer la résistance interne, on mesure la variation de courant et de tension de la cellule en décharge comme suit:
$$R_i \approx \frac{\Delta V}{\Delta I}$$
### Capacité
La capacité d'une batterie est la quantité d'électron en $Ah$ pouvant être accumulées dans la plage d'opération réversibles de la cellule entre sa tension maximale et minimale. 

### Tension nominale
La tension qu'aurait une cellule à la même quantité d'énergie si son potentiel n'était pas affecté par l'état de charge.
![](Images/Pasted%20image%2020250701105804.png)

L'énergie contenue dans une cellule est donc défini comme suit:
$$V_{nom}Q_0=\iint{dVdQ}$$
Il est possible de l'approximer géométriquement avec la courbe:
![](Images/Pasted%20image%2020250701110337.png)

