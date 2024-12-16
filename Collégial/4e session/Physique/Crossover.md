### Type: 
#### Actif
Un crossover passif est placé entre le pre-amp et l'amp, il prend le signal au niveau de ligne et applique plusieurs filtres pour isoler certaines fréquences et les envoyer au bon driver. Chaque driver a son ampli indépendant et on peut ainsi ajuster la balance. Un crossover actif permet un meilleur contrôle sur les différentes fréquences.
#### Passif
Un crossover passif est situé entre l'amplificateur et les drivers. Il applique des filtres sur un signal déjà amplifié et isole certaines fréquences et les envoie au bon driver. Pour ajuster la balance avec un crossover passif, on utiliser des résistances en série avec les drivers.

![Pasted image 20240210101526](Pasted%20image%2020240210101526.png)

#### 2-way
Un crossover 2-way sépare le signal en deux signaux indépendants. Il utilise un filtre low-pass pour le woofer et un filtre high-pass pour le tweeter.
#### 3-way
Un crossover 3-way sépare le signal en trois signaux indépendants. Il utilise un filtre low-pass pour le woofer et un filtre high-pass pour le tweeter et un filtre band-pass pour le mid range.

### Filtres
#### Filtre low-pass
Un filtre low-pass laisse seulement passer les basses fréquences à l'aide d'un inducteur en série et une résistance en parallèle.
![Pasted image 20240210103959](Pasted%20image%2020240210103959.png)
#### Filtre high-pass
Un filtre low-pass laisse seulement passer les hautes fréquences avec un condensateur en série et une résistance en parallèle.
![Pasted image 20240210102541](Pasted%20image%2020240210102541.png)
#### Filtre band-pass
Un filtre band-pass est composé d'un filtre low-pass et d'un filtre high-pass en série pour isoler un certain intervalle de fréquence.
#### Ordre des filtres
Les trois types de filtres peuvent avoir un certain ordre. Il s'agit du *nombre* de filtre en série. Plus un filtre a un ordre élevé, plus il va couper rapidement les fréquences non voulues.
![Pasted image 20240210102306](Pasted%20image%2020240210102306.png)
#### Type de filtres:

##### Filtre Butterworth 
![Pasted image 20240210102823](Pasted%20image%2020240210102823.png)
![Pasted image 20240210102843](Pasted%20image%2020240210102843.png)

Aucune oscillation dans le passband mais plus lent
##### Filtre Chebyshev
![Pasted image 20240210102754](Pasted%20image%2020240210102754.png)
Présence d'oscillation mais très rapide

$\omega_0 = \frac{1}{\sqrt{LC}}$
