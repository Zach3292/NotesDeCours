# Cours 2

Introduction au tableau avec Numpy

Le code si-dessous importe la library numpy avec le "surnom" np


```python
import numpy as np
```

Le code si-dessous montre qu'un tableau numpy n'est pas une matrice puisqu'on peut ajouter une constante

Il y a aussi des exemples de calculs sur les arrays (tableaux)

*Important: la multiplication d'array n'est pas une multiplication matricielle*

On peut aussi faire des divisions ou des puissances avec des arrays


```python
a = np.array([1, 2, 3, 4])
b = np.array([5, 6, 7, 8])

add = a + 10
print("Addition", add)

diff = b - a
print("Soustraction", diff)

mult = a * b
print("Multiplication", mult)

div = b / a
print("Division", div)

power = a ** 2
print("Exposant", power)

powerBetweenArray = a ** b
print("Exposant entre arrays", powerBetweenArray)
```

    Addition [11 12 13 14]
    Soustraction [4 4 4 4]
    Multiplication [ 5 12 21 32]
    Division [5.         3.         2.33333333 2.        ]
    Exposant [ 1  4  9 16]
    Exposant entre arrays [    1    64  2187 65536]


On peut accéder à des éléments particulier d'un array
L'indice commence à 0 toujours


```python
print("Premier élément", a[0])
print("Deuxième élément", a[1])
print("Troisième élément", a[2])
print("Dernier élément", a[-1])
print("Avant dernier élément", a[-2])
```

    Premier élément 1
    Deuxième élément 2
    Troisième élément 3
    Dernier élément 4
    Avant dernier élément 3


Il est possible de savoir la dimension et la forme d'un array
Un array peut avoir une infinité de dimension


```python
a = np.array([[1, 2, 3, 4], 
              [5, 6, 7, 8]])
```


```python
print(a)
print("Dimension", a.shape)
print("Nombre de lignes", a.shape[0])
print("Nombre de colonnes", a.shape[1])
```

    [[1 2 3 4]
     [5 6 7 8]]
    Dimension (2, 4)
    Nombre de lignes 2
    Nombre de colonnes 4


On peut accéder à des éléments comme avec une array 1d


```python
print("Première ligne, deuxième colonne", a[0, 1])
print("Deuxième ligne, troisième colonne", a[1, 2])
```

    Première ligne, deuxième colonne 2
    Deuxième ligne, troisième colonne 7


Il est possible d'échelonner une matrice avec python en sélectionnant tous les éléments d'une ligne en particulier *(la même chose peut être fait avec les colonnes)*
*sans loop c'est long pour rien*


```python
mat = np.array([2, 1, 2](2,%201,%202)).astype(float)
print("Avant échelonnage\n", mat)

mat[0,:] = mat[0,:] / mat[0,0]

mat[1,:] = mat[1,:] - mat[1,0] * mat[0,:]
mat[2,:] = mat[2,:] - mat[2,0] * mat[0,:]

mat[1,:] = mat[1,:] / mat[1,1]

mat[2,:] = mat[2,:] - mat[2,1] * mat[1,:]

mat[2,:] = mat[2,:] / mat[2,2]

print("Après échelonnage\n", mat)
```

    Avant échelonnage
     [[2. 1. 2.]
     [3. 4. 1.]
     [3. 3. 3.]]
    Après échelonnage
     [[ 1.   0.5  1. ]
     [ 0.   1.  -0.8]
     [ 0.   0.   1. ]]


Il est possible de créer une array rempli de 0 ou de 1 automatiquement

*On peut aussi faire n'importe quelle valeur*

Il y a différente possibilité de création d'array


```python
zero = np.zeros((3, 3))
print("Matrice de zéros\n", zero)
one = np.ones((3, 3))
print("Matrice de uns\n", one)
ten = np.full((3, 3), 10)
print("Matrice de dix\n", ten)
arrange = np.arange(0, 10, 2)
print("Matrice de 0 à 10 par pas de 2\n", arrange)
linspace = np.linspace(0, 10, 5)
print("Matrice de 0 à 10 avec 5 valeurs\n", linspace)
random = np.random.random((3, 3))
print("Matrice aléatoire entre 0 et 1\n", random)
print("Matrice aléatoire entre -50 et 50\n", random * 100 - 50)
```

    Matrice de zéros
     [[0. 0. 0.]
     [0. 0. 0.]
     [0. 0. 0.]]
    Matrice de uns
     [[1. 1. 1.]
     [1. 1. 1.]
     [1. 1. 1.]]
    Matrice de dix
     [[10 10 10]
     [10 10 10]
     [10 10 10]]
    Matrice de 0 à 10 par pas de 2
     [0 2 4 6 8]
    Matrice de 0 à 10 avec 5 valeurs
     [ 0.   2.5  5.   7.5 10. ]
    Matrice aléatoire entre 0 et 1
     [[0.3160573  0.63722412 0.80948516]
     [0.41330353 0.81000961 0.40993087]
     [0.21653948 0.838972   0.07724055]]
    Matrice aléatoire entre -50 et 50
     [[-18.39427009  13.72241153  30.94851645]
     [ -8.66964689  31.00096122  -9.00691305]
     [-28.34605243  33.89720048 -42.27594543]]


Il est possible de faire des graphiques avec la library matplolib


```python
import matplotlib.pyplot as plt
import numpy as np
import math
```

L'ordinateur représente des données discrètes seulement
Il est possible de créer un fonction et de la représenter avec une certaine précision


```python
x = np.linspace(-2 * math.pi , 2 * math.pi, 100)
y = np.cos(x)

plt.plot(x, y)
plt.rcdefaults
plt.xlabel('x')
plt.ylabel('cos(x)')
plt.title('Cosinus')
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_19_0.png)
    


il est possible de sauvegarder un graphique dans le même répertoire que le script python


```python
#plt.savefig('cosinus.png')
```

# Cours 3
Boucles et conditions

**Boucle**

Dans une boucle for, le range() fait rouler la boucle le nombre de fois inscrit en paranthèse et l'indice commence à zéro et fini au nombre d'itération -1

On peut aussi lui indiqué un interval


```python
a = np.random.random(5)

for i in range(a.shape[0]):
    print("L'élément", i, "est égal à:", a[i])
print("")
for i in range(1, a.shape[0] -1):
    print("L'élément", i, "est égal à:", a[i])
```

    L'élément 0 est égal à: 0.03044713672859145
    L'élément 1 est égal à: 0.5863520101975568
    L'élément 2 est égal à: 0.26587621139932616
    L'élément 3 est égal à: 0.7713697451664685
    L'élément 4 est égal à: 0.04472597297355263
    
    L'élément 1 est égal à: 0.5863520101975568
    L'élément 2 est égal à: 0.26587621139932616
    L'élément 3 est égal à: 0.7713697451664685


On peut énumérer les éléments d'un array


```python
A = np.random.random(3)

for i, a in enumerate(A):
    print("L'élément", i, "est égal à:", a)
```

    L'élément 0 est égal à: 0.9818626412431939
    L'élément 1 est égal à: 0.454826842578709
    L'élément 2 est égal à: 0.31118361550558904


On peut imbriquer des boucles


```python
A = np.random.random((3, 3))

for line in range(A.shape[0]):
    for col in range(A.shape[1]):
        print("L'élément", line, col, "est égal à:", A[line, col])
```

    L'élément 0 0 est égal à: 0.1598293075783883
    L'élément 0 1 est égal à: 0.022167037203243645
    L'élément 0 2 est égal à: 0.2172339228182406
    L'élément 1 0 est égal à: 0.1545609526605457
    L'élément 1 1 est égal à: 0.6501989737375782
    L'élément 1 2 est égal à: 0.10228175140422358
    L'élément 2 0 est égal à: 0.46118393698976723
    L'élément 2 1 est égal à: 0.6255895379411186
    L'élément 2 2 est égal à: 0.3328213307680341



```python
a = np.arange(20)

b = np.zeros_like(a)

for i in range(1, a.shape[0] - 1):
    b[i] = a[(i-1)] + a[i] + a[(i+1)]
print(b)
```

    [ 0  3  6  9 12 15 18 21 24 27 30 33 36 39 42 45 48 51 54  0]


**Conditions**
Il faut utiliser les blocs *if, else, et elif*

*Le np.where(condition, vrai, faux) peut être utilisé comme shortcut pour des conditions simples*


```python
a = np.random.random(10)
print(a)
b = np.zeros_like(a)

for i in range(a.shape[0]):
    if a[i] > 0.75:
        b[i] = 2
    elif a[i] > 0.5:
        b[i] = 1
    else:
        b[i] = 0
print(b)
#Cheeky shortcut
print(np.where(a > 0.5, 1, 0))
```

    [0.87339999 0.24116274 0.98282112 0.81669739 0.04446825 0.62129335
     0.1559856  0.06841107 0.95553035 0.12502565]
    [2. 0. 2. 2. 0. 1. 0. 0. 2. 0.]
    [1 0 1 1 0 1 0 0 1 0]



```python
import numpy as np
randomArray = np.random.random(20)   #On crée un tableau de 20 nombres aléatoires
print(randomArray)

resultArray = np.zeros_like(randomArray)   #On crée un tableau de 20 zéros

for i in range(resultArray.shape[0]):
    
    resultArray[i] = np.min(randomArray)          #On ajoute le minimum dans le résultat

    randomArray = np.delete(randomArray, np.argmin(randomArray))

print(resultArray)



```

    [0.69073797 0.66622018 0.74111385 0.29880974 0.95323699 0.45749508
     0.670586   0.80422707 0.58741376 0.4727292  0.71846897 0.59811747
     0.91013118 0.00204781 0.36040526 0.38696291 0.47901077 0.28416137
     0.28816433 0.78175808]
    [0.00204781 0.28416137 0.28816433 0.29880974 0.36040526 0.38696291
     0.45749508 0.4727292  0.47901077 0.58741376 0.59811747 0.66622018
     0.670586   0.69073797 0.71846897 0.74111385 0.78175808 0.80422707
     0.91013118 0.95323699]


On peut créer une copy d'un array avec np.copy(array à copier)
np.isclose(nombre, 0.0) regarde si une valeur décimale est égale jusqu'à la précision de l'ordinateur, exemple: un nombre très proche de zéro

# Cours 4

**Dérivation numérique**

*Dérivation numérique d'une fonction continue*

Du continu au discret



Il faut définir trois solutions pour approximer la dérivée (voir formule dans cahier)

#### Forward difference
$$f'(a) \approx \frac{f(a+h)-f(a)}{h}$$
#### Backward difference
$$f'(a) \approx \frac{f(a)-f(a-h)}{h}$$
#### Central difference
$$f'(a) \approx \frac{f(a+h)-f(a-h)}{2h}$$



```python
import numpy as np
import matplotlib.pyplot as plt

dydx_exact = -1.0

f = lambda x: np.cos(x)

h = np.array([1, 0.1, 0.01, 0.001, 0.0001])

for i in range(h.shape[0]):
    dydx_approx = (f(np.pi/2 + h[i]) - f(np.pi/2 - h[i])) / (2 * h[i])
    print("Approximation avec h =", h[i], ":", dydx_approx)
    erreur = np.abs(dydx_exact - dydx_approx)
    print("Erreur avec h =", h[i], ":", erreur)

```

    Approximation avec h = 1.0 : -0.8414709848078965
    Erreur avec h = 1.0 : 0.1585290151921035
    Approximation avec h = 0.1 : -0.9983341664682823
    Erreur avec h = 0.1 : 0.0016658335317176753
    Approximation avec h = 0.01 : -0.9999833334166673
    Erreur avec h = 0.01 : 1.666658333265847e-05
    Approximation avec h = 0.001 : -0.9999998333332315
    Erreur avec h = 0.001 : 1.6666676849741435e-07
    Approximation avec h = 0.0001 : -0.9999999983332231
    Erreur avec h = 0.0001 : 1.6667769386913278e-09



```python
dydx_exact = -2

x = 0

f = lambda x: 3*x**3 + 5*x**2 - 2*x - 7

h = 0.01

dydx_approx = (f(x + h) - f(x - h)) / (2 * h)
print("Approximation avec h =", h, ":", dydx_approx)
erreur = np.abs(dydx_exact - dydx_approx)
print("Erreur avec h =", h, ":", erreur)
```

    Approximation avec h = 0.01 : -1.9997000000000043
    Erreur avec h = 0.01 : 0.0002999999999957481


*Dérivation d'ordre supérieur*

Pour y arriver, on fait la central difference de la centrale difference


```python
f = lambda x: np.cos(x)

x = 0

h = 0.01

def derivee(f, h, ordre = 1):
    temp = lambda x: (f(x + h) - f(x - h)) / (2 * h)

    if ordre > 1:
        ordre -= 1
        temp = derivee(temp, h, ordre)

    return temp

f_prime = derivee(f, h, 1)

f_prime_prime = derivee(f, h, 2)

print("Approximation de la dérivée de cos(x) en 0 avec h =", h, ":", f_prime(x))
print("Approximation de la dérivée seconde de cos(x) en 0 avec h =", h, ":", f_prime_prime(x))
```

    Approximation de la dérivée de cos(x) en 0 avec h = 0.01 : 0.0
    Approximation de la dérivée seconde de cos(x) en 0 avec h = 0.01 : -0.9999666671112184


Une meilleure méthode est avec les polynomes de Taylor
#### Polynôme de Taylor
$$ T_n (x) = \sum_{k=0}^{n} \frac{f^{(k)} (a)}{k!} (x-a)^k$$



```python
f = lambda x: 3*np.exp(x) / (x**2 + x + 1)

a = 0
h = 0.001

x_num = np.linspace(-3, 3, 300)
y_f = f(x_num)

a0 = f(a)
a1 = derivee(f, h, 1)(a)
a2 = derivee(f, h, 2)(a)
a3 = derivee(f, h, 3)(a)

T3 = lambda x: a0 + a1 * x + a2/2 * x**2 + a3/6 * x**3

y_T3 = T3(x_num)

plt.plot(x_num, y_f, label = 'f(x)')
plt.plot(x_num, y_T3, label = 'T3(x)')
plt.xlabel('x')
plt.ylabel('y')
plt.xlim(-3, 3)
plt.ylim(0, 5)
plt.title('Approximation de f(x) par T3(x) en 0')
plt.legend()
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_41_0.png)
    


# Cours 5

**Dérivation d'une fonction discrète**

Identique qu'une dérivée continue, il faut juste mettre h = 1 et a doit être un entier inclu entre le début et la fin du tableau


```python
import numpy as np
import matplotlib.pyplot as plt

data = np.genfromtxt('dataset/elevation.txt')

h = 1

dydx = np.zeros_like(data)

# Exclusion de la première et dernière valeur pour évité les erreurs d'index
for a in range(h, data.shape[0] - h):
    dydx[a] = (data[a + h] - data[a - h]) / (2 * h)

dydx[0] = (data[0 + h] - data[0]) / h
dydx[-1] = (data[-1] - data[-1 - h]) / h

plt.plot(data, label = 'Altitude')
plt.title('Altitude (m) en fonction du temps (s)')
plt.show()
plt.plot(dydx, label = 'Vitesse')
plt.title('Vitesse verticale (m/s) en fonction du temps (s)')
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_44_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_44_1.png)
    


Fait une approximation pour les dérivées d'ordres supérieures parce que le plus petit h n'est pas nécessairement 1 plus on augmente dans les ordres


```python
def deriveeDiscrete(data, ordre = 1):
    h = 1

    temp = np.zeros_like(data)

    # Exclusion de la première et dernière valeur pour évité les erreurs d'index
    for a in range(h, data.shape[0] - h):
        temp[a] = (data[a + h] - data[a - h]) / (2 * h)

    temp[0] = (data[0 + h] - data[0]) / h
    temp[-1] = (data[-1] - data[-1 - h]) / h

    if ordre > 1:
        ordre -= 1
        temp = deriveeDiscrete(temp, ordre)

    return temp
```

*Meilleure version du code:*


```python
import numpy as np
import matplotlib.pyplot as plt

data = np.genfromtxt('dataset/elevation.txt')

h = 1

dydx = deriveeDiscrete(data)

plt.plot(data, label = 'Altitude')
plt.title('Altitude (m) en fonction du temps (s)')
plt.show()
plt.plot(dydx, label = 'Vitesse')
plt.title('Vitesse verticale (m/s) en fonction du temps (s)')
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_48_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_48_1.png)
    


## Interlude

Filtre moyenneur: pour chaque position d'un array on fait la moyenne de m nombre de valeur avant et après. Permet de diminuer les grandes fluctuations de valeur




```python
data = np.genfromtxt('dataset/elevation.txt')

m = 5

data_moyen = np.zeros_like(data)

for i in range(data_moyen.shape[0]):
    debut = max(0, i - m)
    fin = min(data_moyen.shape[0]-1, i + m)
    data_moyen[i] = np.mean(data[debut:fin+1])

plt.plot(data_moyen)
plt.title('Altitude (m) en fonction du temps (s) (m = %i)' % m)
plt.show()
plt.plot(deriveeDiscrete(data_moyen))
plt.title('Vitesse verticale (m/s) en fonction du temps (s) (m = %i)' % m)
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_50_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_50_1.png)
    


Numpy a sa propre fonction pour dérivée des fonctions discrètes 
    (np.gradient)


```python
data = np.genfromtxt('dataset/elevation.txt')

m = 5

data_moyen = np.zeros_like(data)

for i in range(data_moyen.shape[0]):
    debut = max(0, i - m)
    fin = min(data_moyen.shape[0]-1, i + m)
    data_moyen[i] = np.mean(data[debut:fin+1])

derivee = np.gradient(data_moyen)

plt.plot(derivee)
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_52_0.png)
    


## Manipulation d'image

On utilise un autre library pour les images soit scikit

On peut changer les valeurs d'une image comme un array numpy

On peut aussi sauvegarder un fichier avec scikit


```python
import numpy as np
import matplotlib.pyplot as plt
import skimage.io as ski

image1 = ski.imread('dataset/kanye.png')
ski.imshow(image1)
ski.show()
image2 = image1 * 0.5
ski.imshow(image2.astype(np.uint8), cmap = 'gray')
ski.show()
#ski.imsave('kanye2.png', image2.astype(np.uint8))
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_55_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_55_1.png)
    


Défi trouver Kanye


```python
import numpy as np
import matplotlib.pyplot as plt
import skimage.io as ski

kanye = ski.imread('dataset/kanye.png')
corgis = ski.imread('dataset/corgis.png')

for i in range(corgis.shape[0]):
    for j in range(corgis.shape[1]):
        if corgis[i, j] == kanye[0, 0]:
            if np.all(corgis[i:i+kanye.shape[0], j:j+kanye.shape[1]] == kanye):
                corgis[i:i+kanye.shape[0], j:j+kanye.shape[1]] = 0
                

ski.imshow(corgis)
ski.show()

                    
                    
            
```

    /var/folders/f3/qh_0g60x7fxc1nzlkd1kqpr40000gn/T/ipykernel_44754/3328036953.py:11: DeprecationWarning: elementwise comparison failed; this will raise an error in the future.
      if np.all(corgis[i:i+kanye.shape[0], j:j+kanye.shape[1]] == kanye):



    
![png](Note%20de%20cours_files/Note%20de%20cours_57_1.png)
    


Défi compression d'image


```python
corgis = ski.imread('dataset/corgis.png')

n = 10

for i in range(int(corgis.shape[0]/n)):
    for j in range(int(corgis.shape[1]/n)):
        corgis[i*n:(i+1)*n, j*n:(j+1)*n] = np.mean(corgis[i*n:(i+1)*n, j*n:(j+1)*n])

ski.imshow(corgis.astype(np.uint8), cmap = 'gray')
ski.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_59_0.png)
    



```python
import numpy as np
import matplotlib.pyplot as plt
import skimage.io as ski

plage = ski.imread('dataset/plage_gray.png')
corgis = ski.imread('dataset/corgis_blackbg_gray.png')

for i in range(plage.shape[0]):
    for j in range(plage.shape[1]):
        if corgis[i, j] != 0:
            plage[i, j] = corgis[i, j]

ski.imshow(plage, cmap = 'gray')
ski.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_60_0.png)
    


# Cours 6

**Dérivation en deux dimensions**

Il faut juste dériver chaque variable indépendament

Le gradient est un array 3D qui combine les deux dérivées partielles
La norme du gradient est la variation de l'array 2D originale

#### Dérivée deux dimensions
1. Il faut calculer la dérivée partielle de chaque dimension soit:
	$$ \frac{\delta f(x, y)}{\delta x} et \frac{\delta f(x, y)}{\delta y}$$
2. Ensuite, il faut créer un vecteur ayant comme composantes les deux dérivées partielles. Celui-ci s'appelle le gradient
	$$\vec{G} = \left[ \frac{\delta f(x, y)}{\delta x} \;\;\; \frac{\delta f(x, y)}{\delta y}\right]$$
3. La norme du gradient correspond à la dérivée deux dimensions de la fonctions
		$$ ||G|| = \sqrt{{\left(\frac{\delta f(x, y)}{\delta x}\right)}^2+{\left(\frac{\delta f(x, y)}{\delta y}\right)}^2}$$



```python
import numpy as np
import skimage.io as ski

a = np.zeros((256, 512))

for i in range(a.shape[0]):
    for j in range(a.shape[1]):
        a[i, j] = i**2 + j**2

dadx = np.gradient(a, axis = 1)
dady = np.gradient(a, axis = 0)

gradient = np.zeros((256, 512, 2))
gradient[:, :, 0] = dadx
gradient[:, :, 1] = dady

norme = np.zeros_like(a)

norme = np.sqrt(dadx**2 + dady**2)

ski.imshow((norme*255/norme.max()).astype(np.uint8), cmap = 'gray')
ski.show()


```


    
![png](Note%20de%20cours_files/Note%20de%20cours_63_0.png)
    


### Détection de contour d'objet

L'array de la norme du gradient d'une image correspond aux contours d'une image


```python
import numpy as np
import skimage.io as ski

seuil = 0.12

corgis = ski.imread('dataset/corgis.png')
dadx = np.gradient(corgis, axis = 1)
dady = np.gradient(corgis, axis = 0)

gradient = np.zeros((corgis.shape[0], corgis.shape[1], 2))
gradient[:, :, 0] = dadx
gradient[:, :, 1] = dady

norme = np.zeros_like(corgis)

norme = np.sqrt(dadx**2 + dady**2)

norme = norme / norme.max()
norme = norme > seuil
norme = norme * 255

ski.imshow(norme.astype(np.uint8), cmap = 'gray')
ski.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_65_0.png)
    


# Cours 7

Filtre moyenneur en 2d:
utile pour réduire le bruit dans les contours

#### Filtre moyenneur
Le filtre moyenneur d'une image se calcule comme cela:
$$T_m (i,\ j) = \frac{1}{(2m+1)^2}\sum^{i+m}_{k=i-m}{\sum^{j+m}_{l=j-m}}{T(k,\ l)}$$
L'image résultante sera flou comparé à l'original


```python
import numpy as np
import skimage.io as ski

corgis = ski.imread('dataset/corgis.png')
output = np.zeros_like(corgis)

m = 3

for i in range(corgis.shape[0]):
        for j in range(corgis.shape[1]):
            debut_i = max(0, i - m)
            fin_i = min(corgis.shape[0]-1, i + m)
            debut_j = max(0, j - m)
            fin_j = min(corgis.shape[1]-1, j + m)
            output[i, j] = np.mean(corgis[debut_i:fin_i+1, debut_j:fin_j+1])

ski.imshow(output, cmap = 'gray')
ski.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_68_0.png)
    


# Cours 8 et 9
Intégration numérique

Pour pouvoir utiliser le théorème fondamental de l'intégration, il faut pouvoir trouver des primitives de fonctions malgré le fait que pluseirus fonctions n'ont pas de primitive
Voici une fonction utilisée en exemple qui respecte le théorème fondamental:$$f(x) = \sin{0.2x} + \sin{2x} + 1$$

Trois méthode seront utilisées:
1. La somme de Riemann
2. La méthode des trapèzes
3. La méthode de Simpson

### Somme de Riemann
$$\Delta x = \frac{b-a}{n}$$
$$\sum_{k=1}^{n}{f(x^{*}_k)\Delta x}$$

Pour l'utiliser, on définit trois positions de $x_k^*$:
* L'extrémité gauche: $x_k^* = x_{k-1}$
* Le centre du sous intervalle: $x_k^* =\frac{x_{k-1}+x_k}{2}$
* L'extrémité droite du sous intervalle: $x_k^* = x_k$

Le centre est la méthode à privilégier lors d'intégration numérique lorsque possible


```python
import numpy as np
import matplotlib.pyplot as plt

f = lambda x: np.sin(0.2*x) + np.sin(2*x) + 1
primitive = lambda x: -5 * np.cos(0.2*x) + 0.5 * np.sin(2*x) + x

a = np.pi /2
b = 3 * np.pi / 2
n = 10
dx = (b - a) / n

X = np.linspace(a, b, 1000)
Y = f(X)

x = np.linspace(a, b, n + 1)

x_centre = (x[:-1] + x[1:])/2
y_centre = f(x_centre)

integrale = np.sum(y_centre) * dx
print("Intégrale avec", n, "rectangles:", integrale)
erreur = np.abs(integrale - primitive(b) + primitive(a))
print("Erreur avec", n, "rectangles:", erreur)

plt.plot(X, Y, 'b')
plt.plot(x_centre, y_centre, 'b.', markersize = 10)
plt.bar(x_centre, y_centre, width = dx, align = 'center', edgecolor = 'b', alpha = 0.2)
plt.title('Méthode des rectangles au centre')
plt.show()
```

    Intégrale avec 10 rectangles: 4.95824778664859
    Erreur avec 10 rectangles: 0.000298813045395363



    
![png](Note%20de%20cours_files/Note%20de%20cours_72_1.png)
    


Intégration numérique (suite)

Avec une fonction discrète, on ne peut pas évaluer le rectangle du centre puisqu'il n'y a pas de valeur associé au centre. Il est possible de regrouper les sous-intervalles en groupe de deux pour créer un *point-milieu* artificiel. Par contre, on a la moitié des sous-intervalles précédentes.

### Analyse de l'erreur

$$R^g_n(f) = \sum^n_{i=1}{f(x_i-1)\Delta x}$$
$$R^d_n(f) = \sum^n_{i=1}{f(x_i)\Delta x}$$
$$R^c_n(f) = \sum^n_{i=1}{f\left(\frac{x_i-1 + x_i}{2}\right)\Delta x}$$

Les erreurs d'approximation associées aux sommes de Riemann sont égales à:

$$E^g_{R_n}(f) = \left| \int^b_a{f(x)dx} - R^g_n(f) \right|$$
$$E^d_{R_n}(f) = \left| \int^b_a{f(x)dx} - R^d_n(f) \right|$$
$$E^c_{R_n}(f) = \left| \int^b_a{f(x)dx} - R^c_n(f) \right|$$

Les erreurs auront un valeur maximale de:

$$E^g_{R_n}(f) \leq \frac{(b-a)^2}{2n}M_1$$
$$E^d_{R_n}(f) \leq \frac{(b-a)^2}{2n}M_1$$
$$E^c_{R_n}(f) \leq \frac{(b-a)^3}{24n^2}M_2$$

Où $|f'(x)| \leq M_1 et |f''(x)| \leq M_2$ pour $x \in [a,b]$

Autrement dit, $M_1$ correspond à la valeur maximale de $|f'(x)|$ et $M_2$ correspond à la valeur maximale de $|f''(x)|$ pour $x \in [a,b]$


```python
import numpy as np
import matplotlib.pyplot as plt

f = lambda x: np.sin(0.2*x) + np.sin(2*x) + 1
primitive = lambda x: -5 * np.cos(0.2*x) + 0.5 * np.sin(2*x) + x

a = np.pi /2
b = 3 * np.pi / 2


X = np.linspace(a, b, 1000)
Y = f(X)

dydx = np.gradient(Y, (b-a)/1000)
d2ydx2 = np.gradient(dydx, (b-a)/1000)

M1 = max(abs(dydx))
M2 = max(abs(d2ydx2))

n_max = 25

borne_gd = np.zeros((n_max, 1))
borne_centre = np.zeros((n_max, 1))

for i in range(1, n_max):
    borne_gd[i] = (b - a)**2 * M1 / (2 * i)
    borne_centre[i] = (b - a)**3 * M2 / (24 * i**2)

plt.plot(borne_gd[1:], label = 'Borne méthode des rectangles à gauche')
plt.plot(borne_centre[1:], label = 'Borne méthode des rectangles au centre')
plt.show()

```


    
![png](Note%20de%20cours_files/Note%20de%20cours_76_0.png)
    


### Méthode des trapèzes

Comme la somme de Riemann mais avec des trapèzes au lieu des rectangles

Voici la règle:

$$T_n(f)=\sum^n_{k=1}{\frac{f(x_{k-1})+f(x_k)}{2}\Delta x} = \frac{\Delta x}{2}\sum^n_{k=1}{f(x_{k-1})+f(x_k)}$$
Où: $$\Delta x = \frac{b-a}{2}$$
Aussi, il est intéressant de savoir que:
$$T_n(f)=\frac{R^g_n(f) + R^d_n(f)}{2}$$


```python
f = lambda x: np.sin(0.2*x) + np.sin(2*x) + 1
primitive = lambda x: -5 * np.cos(0.2*x) + 0.5 * np.sin(2*x) + x

a = np.pi /2
b = 3 * np.pi / 2
n = 10
dx = (b - a) / n

X = np.linspace(a, b, 1000)
Y = f(X)

x = np.linspace(a, b, n + 1)
y = f(x)

integrale = 0
for i in range(n):
    integrale += (y[i] + y[i+1]) / 2 * dx
    plt.fill_between([x[i], x[i+1]], [y[i], y[i+1]])

print("Intégrale avec", n, "trapèzes:", integrale)

erreur = np.abs(integrale - primitive(b) + primitive(a))

print("Erreur avec", n, "trapèzes:", erreur)

plt.plot(x, y, 'b.', markersize = 10)
plt.plot(X, Y, 'Magenta')
plt.show()
```

    Intégrale avec 10 trapèzes: 4.957351377004142
    Erreur avec 10 trapèzes: 0.0005975965990527854



    
![png](Note%20de%20cours_files/Note%20de%20cours_78_1.png)
    


Pour la méthode des trapèzes:
$$E_{T_n}(f) = \left| \int^b_a{f(x)dx} - {T_n}(f) \right|$$
$$E_{T_n}(f) \leq \frac{(b-a)^3}{12n^2}M_2$$

Très similaire à la méthode de Riemann mais avec une erreur d'approximation deux fois plus grande, beaucoup plus répendu que la méthode de Riemann

### Méthode de Simpson
Pour chaque sous-intervalle, on va définir un polynôme quadratique

Pour une fonction discrète, il faut faire comme avec Riemann et évaluer au point initial, final et central du sous-intervalle.

Pour trouver un point central il faut doubler la largeur des sous-intervalles


```python
f = lambda x: np.sin(0.2*x) + np.sin(2*x) + 1

a = np.pi /2
b = 3 * np.pi / 2
n = 10

X = np.linspace(a, b, 1000)
Y = f(X)

x = np.linspace(a, b, 2*n + 1)
y = f(x)

for i in range(n):
    x_local = x[2*i:2*i+3]
    y_local = f(x_local)
    coeff = np.array([[x_local[0]**2, x_local[0], 1],
                      [x_local[1]**2, x_local[1], 1],
                      [x_local[2]**2, x_local[2], 1]])
    const = np.array([y_local[0], y_local[1], y_local[2]])
    [A, B, C] = np.linalg.solve(coeff, const)

    x_local_plot = np.linspace(x_local[0], x_local[2], 20)
    f_local_plot = lambda x: A*x**2 + B*x + C
    y_local_plot = f_local_plot(x_local_plot)
    plt.plot(x_local_plot, y_local_plot, 'g')
    plt.plot(x_local, y_local, 'b.', markersize = 10)

plt.plot(X, Y, 'b')
plt.show()

```


    
![png](Note%20de%20cours_files/Note%20de%20cours_81_0.png)
    


Formule simplifiée de la méthode de Simpson *fuck la preuve*:
$$S_n(f) = \frac{\Delta x}{6}\sum^n_{k=1}{\left(f(x_{k-1}) + 4 f(x_{k-\frac{1}{2}}) + f(x_k)\right)}$$

$$S_n(f) = \frac{\Delta x}{6}\left(\sum^n_{k=1}{\left(f(x_{k-1})\right)} + 4 \sum^n_{k=1}{\left(f(x_{k-\frac{1}{2}})\right)} + \sum^n_{k=1}{\left(f(x_k)\right)}\right)$$

Analyse de l'erreur de la méthode de Simpson:

$$E_{S_n} \leq \frac{(b-a)^5}{180n^4}M_4$$

où $|f^{(4)}(x)| \leq M_4$



```python
import numpy as np
import scipy.integrate as scpint

f = lambda x: np.sin(0.2*x) + np.sin(2*x) + 1

a = np.pi /2
b = 3 * np.pi / 2
n= 10

dx = (b - a) / n

x = np.linspace(a, b, n+1)
y = f(x)

integrale = np.sum(np.fromiter((
    y[2*i] + 4*y[2*i+1] + y[2*i+2] for i in range(int(n/2))
    ), dtype=float)) * dx / 3 # 3 parce que on a n/2 intervalles au lieu de 2
integrale2 = (dx/6) * np.sum(y[0:-1:2] + 4*y[1::2] + y[2::2]) # avec 2*n+1 points
integrale = scpint.simpson(y, x)
print("Intégrale avec", n, "simpsons:", integrale)

```

    Intégrale avec 10 simpsons: 4.957949130947912


### Intégration numérique efficace avec python

Il existe des fonctions déjà programmées plus efficace que faire le calcul à la main dans la library scipy
```
scipy.integrate.trapezoid() pour la méthode des trapèzes
scipy.integrate.simpson() pour la méthode de Simpson
```


```python
import numpy as np
import scipy.integrate as scpint

f = lambda x: np.sin(0.2*x) + np.sin(2*x) + 1
a = np.pi /2
b = 3 * np.pi / 2
n = 10

x = np.linspace(a, b, n + 1)
y = f(x)

integrale = scpint.trapezoid(y, x)
print("Intégrale avec", n, "trapèzes:", integrale)
integrale = scpint.simpson(y, x)
print("Intégrale avec", n, "simpsons:", integrale)
```

    Intégrale avec 10 trapèzes: 4.957351377004142
    Intégrale avec 10 simpsons: 4.957949130947912


# Cours 10

### Chapitre 4: Les nombres complexes

#### Opérations sur les nombres complexes:

Ils permettent de trouver des solutions à toutes les équations polynomiales
$$i=\sqrt{-1}$$
La forme cartésienne d'un nombre complexe s'écrit:
$$z=a+bi$$

La partie réelle est nommée $Re(z)$ et la partie imaginaire $Im(z)$.




Il est possible de faire des opérations sur les nombres complexes. Pour l'addiction, la soustraction et la multiplication par un scalaire, on agit comme s'il s'agissait d'une vecteur.

Lorsqu'on multiplie deux nombres complexes, on fait de la distributivité comme s'il s'agissait de nombres réels. Un raccourci existe: 
$$z_1z_2 = (a_1a_2-b_1b_2)+(a_1b_2+a_2b_1) \in \mathbb{C} $$

On peut calculer le conjugé d'un nombre complexe:
$$z=a+bi \rightarrow \bar{z} = a-bi$$
Pour diviser un nombre complexe, on multiplie par le conjugé du dénominateur:
$$\frac{z_1}{z_2} = \frac{z_1}{z_2} \times \frac{\bar{z_2}}{\bar{z_2}} = \frac{z_1\bar{z_2}}{z_2\bar{z_2}}$$
Le module d'un nombre complexe se calcule comme un vecteur:
$$|z| = \sqrt{a^2 + b^2}$$

#### Notation polaire des nombres complexes:

Si on divise un nombre complexe par son module, on obtient sa direction

Pour un nombre complexe dit cartésien, $z = a +bi$ où (a, b) sont les composantes du nombre complexe dans le plan d'Argand. Il est possible de transformer ces composantes cartésiennes en composantes polaires (r, $\theta$) et d'obtenir la forme polaire d'un nombre complexe soit:$$r=|z|$$ alors $$z = r\left( \cos{\theta} + i\sin{\theta} \right) $$ où $$|z| = \sqrt{a^2 + b^2}$$
Et:$$\theta = \arctan{\frac{b}{a}}$$
Alors :$$z = \sqrt{a^2 + b^2}\left( \cos{\left(\arctan{\frac{b}{a}}\right)} + i\sin{\left(\arctan{\frac{b}{a}}\right)} \right) $$

On appelle l'angle d'un nombre complexe son argumen, il s'écrit $Arg(z) \in ]-\pi, \pi[$


```python
import numpy as np
import matplotlib.pyplot as plt

nb_complexes = np.array([1+2j, -1+4j, 4+3j, -4, 2-1j, 3+9j, -2+6j, 5])

modules = np.abs(nb_complexes)
nb_complexes_unitaires = nb_complexes / modules
arguments = np.angle(nb_complexes)

fig = plt.figure()
ax = fig.add_subplot(1, 1, 1)
t = np.linspace(0, 2*np.pi, 100)
ax.plot(np.cos(t), np.sin(t), 'r', linewidth = 1)
ax.set_aspect('equal')

plt.scatter(nb_complexes_unitaires.real, nb_complexes_unitaires.imag)
plt.xlabel('Axe réele')
plt.ylabel('Axe imaginaire')
plt.title('Représentation des nombres complexes')
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_89_0.png)
    


Avec la notation polaire on peut simplifer des équations:

$$Arg(\bar{z}) = -Arg(z)$$
$$\bar{z} = r\left(\cos{(-\theta)}+i\sin{(-\theta)}\right)$$

Pour la multiplication et la division de deux nombres complexes:

$$z_1z_2 = r_1r_2\left(\cos{(\theta_1 + \theta_2)}+ i\sin{(\theta_1 + \theta_2)}\right)$$
Et
$$\frac{z_1}{z_2} = \frac{r_1}{r_2}\left(\cos{(\theta_1 - \theta_2)}+ i\sin{(\theta_1 - \theta_2)}\right)$$  

#### Formule de Moivre :


$$z^n = r^n(\cos{n\theta} + i\sin{n\theta})$$
#### Racine n-ième
Utile pour calculer la racine n-ième d'un nbr complexe :

$$z^{\frac{1}{n}} = r^{\frac{1}{n}}\left[\cos{\left(\frac{\theta + 2k\pi}{n}\right)} + i\sin{\left(\frac{\theta + 2k\pi}{n}\right)}\right]$$

où $k  =  0,  1, ...,  n  -  1$

*Pour une racine n-ième, il y a n solutions*


```python
import numpy as np
import matplotlib.pyplot as plt

def get_racines(z, n):
    arg = np.angle(z)
    module = np.abs(z)
    racines = np.zeros(n, dtype = complex)

    for k in range(n):
        angle = (arg + 2*k*np.pi) / n
        racines[k] = (module**(1/n)) * (np.cos(angle) + 1j*np.sin(angle))
    return racines

z = np.array([1])

racines = get_racines(z, 3)

for racine in racines:
    print(racine)
    print(np.abs(racine), "(cos", np.angle(racine), " + i sin", np.angle(racine), ")")

plt.scatter(z.real, z.imag, color = 'r')
plt.scatter(racines.real, racines.imag)
plt.xlabel('Axe réelle')
plt.ylabel('Axe imaginaire')
plt.title('Représentation des racines')
plt.show()



```

    (1+0j)
    1.0 (cos 0.0  + i sin 0.0 )
    (-0.49999999999999983+0.8660254037844387j)
    1.0 (cos 2.0943951023931953  + i sin 2.0943951023931953 )
    (-0.5000000000000004-0.8660254037844384j)
    1.0 (cos -2.094395102393196  + i sin -2.094395102393196 )



    
![png](Note%20de%20cours_files/Note%20de%20cours_92_1.png)
    


#### Formule d'Euler

La formule d'Euler prend un nombre complexe en forme polaire et le transforme en fonction exponentielle comme suit:$$re^{i\theta} = r\left(\cos{\theta} + i\sin{\theta}\right)$$
Ainsi, notre nombre complexe $z=a+bi$ peut s'écrire comme suit:$$z = re^{i\theta} = \sqrt{a^2 + b^2} \cdot e^{i\arctan{\left(\frac{b}{a}\right)}}$$

##### Opérations avec la notation d'Euler:

$$\bar{z} = re^{-i\theta}$$
$$z_1z_2 = r_1r_2e^{i(\theta_1 + \theta_2)}$$
$$\frac{z_1}{z_2} = \frac{r_1}{r_2}e^{i(\theta_1 - \theta_2)}$$

# Cours 11
### Chapitre 5: Séries de Fourier
#### Introduction:
Permet de représenter n'importe quelle fonction comme une sommation de fonctions trigonométriques


#### Forme trigonométrique de période $2\pi$

Soit $f(x)$ une fonction périodique de période $2\pi$: 
$$ f(x) = \frac{a_0}{2} + \sum^{\infty}_{k=1}{\left(a_k\cos{\left(kx\right)} + b_k\sin{\left(kx\right)}\right)}$$

Les coefficients de Fourier sont donnés par:
$$\begin{align}
a_k & = \frac{1}{\pi}\int^{\pi}_{-\pi}{f(x)\cos{\left(kx\right)}dx} \\
b_k & = \frac{1}{\pi}\int^{\pi}_{-\pi}{f(x)\sin{\left(kx\right)}dx}
\end{align}$$

Dans ce cas, toutes les fonctions, soit $f(x)$, $\cos{\left(kx\right)}$ et $\sin{\left(kx\right)}$, sont périodique de période $2\pi$.

Si $f(x)$ n'est pas périodique alors elle sera dupliquée infiniment périodiquement. Le reste de la fonction répétée s'appelle l'extension périodique.

La plupart du temps on va utiliser la **série de Fourier tronquée**:
$$ f(x) = \frac{a_0}{2} + \sum^{n}_{k=1}{\left(a_k\cos{\left(kx\right)} + b_k\sin{\left(kx\right)}\right)}$$



```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.integrate as scpint

n = 1000
x = np.linspace(-np.pi, np.pi, n)

f = np.zeros_like(x)
f = x**3

kmax = 100
Af = np.zeros(kmax + 1)
Bf = np.zeros(kmax + 1)

Af[0] = scpint.simpson(f, x) / np.pi
fFS = Af[0] / 2

for k in range(1, kmax + 1): # On commence à 1 car on a déjà calculé k = 0 et kmax + 1 car on veut inclure kmax
    Af[k] = scpint.simpson(f * np.cos(k * x), x) / np.pi
    Bf[k] = scpint.simpson(f * np.sin(k * x), x) / np.pi
    fFS += Af[k] * np.cos(k * x) + Bf[k] * np.sin(k * x)

plt.plot(x, f, 'b', label = 'f(x)')
plt.plot(x, fFS, 'r', label = 'fFS(x)')
plt.legend()
plt.title('Série de Fourier de f(x) avec %d termes' % kmax)
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_96_0.png)
    


Plus $n$ est grand, plus la précision augmente. 

# Cours 12

#### Forme trigonométrique de période L

Soit $f(x)$ une fonction périodique de période $L$: 
$$ f(x) = \frac{a_0}{2} + \sum^{\infty}_{k=1}{\left(a_k\cos{\left(\frac{2\pi kx}{L}\right)} + b_k\sin{\left(\frac{2\pi kx}{L}\right)}\right)}$$

Les coefficients de Fourier sont donnés par:
$$\begin{align}
a_k & = \frac{2}{L}\int^{L}_{0}{f(x)\cos{\left(\frac{2\pi kx}{L}\right)}dx} \\
b_k & = \frac{2}{L}\int^{L}_{0}{f(x)\sin{\left(\frac{2\pi kx}{L}\right)}dx}
\end{align}$$


```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.integrate as scpint

L = 12
x = np.linspace(0, L, 1000)
n = x.shape[0]
nquart = int(np.floor(n/4))

h = np.zeros_like(x)
h[nquart:3*nquart] = 1

kmax = 50
Ah = np.zeros(kmax + 1)
Bh = np.zeros(kmax + 1)

Ah[0] = 2 * scpint.simpson(h, x) / L
hFS = Ah[0] / 2

for k in range(1, kmax + 1):
    Ah[k] = 2 * scpint.simpson(h * np.cos(k * 2 * np.pi * x / L), x) / L
    Bh[k] = 2 * scpint.simpson(h * np.sin(k * 2 * np.pi * x / L), x) / L
    hFS += Ah[k] * np.cos(k * 2 * np.pi * x / L) + Bh[k] * np.sin(k * 2 * np.pi * x / L)

plt.plot(x, h, 'b', label = 'h(x)')
plt.plot(x, hFS, 'r', label = 'hFS(x)')
plt.legend()
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_99_0.png)
    


Les oscillations avant les discontinuités portent le nom de **phénomène de Gibbs**.

Pour régler ça, on mets des bandes de transitions. En d'autres mots, on ajoute un intervalle qui relie les discontinuités de manière linéaire


```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.integrate as scpint

L = 12
x = np.linspace(0,12,1000)
n = x.shape[0]
nquart = int(np.floor(n/4))

# Largeur de la transition
t_index = 10
t = x[nquart+t_index] - x[nquart]

h2 = np.zeros_like(x)
h2[nquart+t_index:3*nquart-t_index] = 1
h2[nquart-t_index:nquart+t_index] = (1/(2*t)) * x[nquart-t_index:nquart+t_index] + (t-3)/(2*t)
h2[3*nquart-t_index:3*nquart+t_index] = (-1/(2*t)) * x[3*nquart-t_index:3*nquart+t_index] + (9+t)/(2*t)

kmax = 50
Ah2 = np.zeros(kmax+1)
Bh2 = np.zeros(kmax+1)

Ah2[0] = (2/L) * scpint.simpson(h2, x)
h2FS = Ah2[0]/2

for k in range(1,kmax+1):
    Ah2[k] = (2/L) * scpint.simpson(h2 * np.cos(2 * np.pi * k * x / L), x)
    Bh2[k] = (2/L) * scpint.simpson(h2 * np.sin(2 * np.pi * k * x / L), x)
    h2FS += Ah2[k] * np.cos(2*np.pi*k*x/L) + Bh2[k] * np.sin(2*np.pi*k*x/L)

plt.plot(x, h2)
plt.plot(x, h2FS)
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_101_0.png)
    


#### Forme exponentielle

À l'aide de la formule d'Euler, on peut transformer la formule des série de Fourier en formule exponentielle.

$$\begin{align}
f(x) & = \sum^{\infty}_{-\infty}{c_k e^{\frac{2\pi ikx}{L}}} \\
c_k & = \frac{1}{L} \int_0^L{f(x)e^{-\frac{2\pi ikx}{L}}dx}
\end{align}$$


```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.integrate as scpint

L = 12
x = np.linspace(0,12,1000)
n = x.shape[0]
nquart = int(np.floor(n/4))

# Largeur de la transition
t_index = 10
t = x[nquart+t_index] - x[nquart]

h = np.zeros_like(x)
h[nquart+t_index:3*nquart-t_index] = 1
h[nquart-t_index:nquart+t_index] = (1/(2*t)) * x[nquart-t_index:nquart+t_index] + (t-3)/(2*t)
h[3*nquart-t_index:3*nquart+t_index] = (-1/(2*t)) * x[3*nquart-t_index:3*nquart+t_index] + (9+t)/(2*t)

kmax = 50
Ch = np.zeros(kmax+1)

hFS = np.zeros_like(x)

for k in range(-kmax, kmax+1):
    Ch[k] = (1/L) * np.real(scpint.simpson(h*np.exp(-1j*2*np.pi*k*x/L), x))
    hFS += Ch[k] * np.real(np.exp(1j*2*np.pi*k*x/L))

plt.plot(x, h)
plt.plot(x, hFS)
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_103_0.png)
    


# Cours 13

### Chapitre 6: Transformée de Fourier

Pour décomposer une fonction en ses composantes fréquentielles. Avec les séries de Fourier, on supposait qu'un fonction soit périodique. De plus, les séries de Fourier permettent seulement une représentation discrète des fréquences. Elles ignorent ainsi des fréquences intermédiaires. 

#### Introduction

On substitut dans l'équation originale $\Delta\omega = \frac{2\pi}{L}$. Alors:

$$\begin{align}
f(x) & = \sum^{\infty}_{-\infty}{c_k e^{ikx\Delta\omega}} \\
c_k & = \frac{1}{L} \int_0^L{f(x)e^{-ikx\Delta\omega}dx}
\end{align}$$

La transformée de Fourier s'obtient en faisant tendre $L$ vers l'infinie ce qui fera tendre $\Delta\omega$ vers 0.

En faisant les manipulations, on obtient: 

$$ \int{\frac{1}{2\pi}\hat{f}(\omega)e^{i\omega x}d\omega} $$

On dira alors que:

$$\hat{f}(\omega) = \mathcal{F}(f(x)) = \int{f(x)e^{-i\omega x}dx}$$

La formulation précédente nous donne également que 

$$f(x) = \mathcal{F}^{-1}(\hat{f}(\omega)) = \int{\frac{1}{2\pi}\hat{f}(\omega)e^{i\omega x}dw}$$

On dit de cette opération qu'elle est la **transformée de Fourier inverse.**


```python
import numpy as np
import matplotlib.pyplot as plt

A = 5
d = 3

x = np.linspace(-5, 5, 500)
yFT = A * d * np.sinc((x * d/2))

plt.plot(x, yFT)
plt.title('Transformée de Fourier de y(t)')
plt.show()

```


    
![png](Note%20de%20cours_files/Note%20de%20cours_105_0.png)
    


On appelle le **spectre d'amplitude** la fonction $\left|\hat{f}(\omega)\right|$ et le **spectre de phase** la fonction $\Phi(\omega)$ qui correspond à l'argument de $\hat{f}(\omega)$.


```python
import numpy as np
import matplotlib.pyplot as plt

A = 5
d = 3
w = np.linspace(-5, 5, 500)
yFT = A * d * np.sinc(w * d/2)

plt.plot(w, np.abs(yFT))
plt.title('Spectre d\'amplitude')
plt.show()

plt.plot(w, np.angle(yFT))
plt.title('Spectre de phase')
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_107_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_107_1.png)
    


Si on multiplie l'amplitude et la phase on obtient la transformé de Fourier

$$\hat{f}(\omega) = \left|\hat{f}(\omega)\right|e^{i\Phi(\omega)}$$

Le résultat de la transformé de Fourier est une fonction complexe.

#### Existence et propriétés de la transformée de Fourier

Pour qu'un fonction possède une transformée de Fourier, elle doit respecté trois propriétés:
1. La fonction présente un **nombre fini de discontinuités** à l'intérieur de tout intervalle fini, et toutes ces discontinuités sont finies $(f(x)\not\rightarrow \pm \infty$ pour tout $ x \in \mathbb{R})$
2. La fonction est **absolument intégrable**, c'est à dire que l'intégrale de la valeur absolue de la fonction est inférieur à l'infinie.
3. Elle possède un **nombre fini d'extremums** à l'intérieur de tout intervalle fini.


On illustre la relation entre une fonction et sa transformée de Fourier comme $f(x) \leftrightarrow \hat{f}(\omega)$

Voici quelques propriétés de la tranformée de Fourier:
1. **Linéarité**: $a_1f_1(x) + a_2f_2(x) \leftrightarrow a_1\hat{f_1}(\omega) + a_2\hat{f_2}(\omega)$

2. **Translation spatiale**: $f(x-a) \leftrightarrow e^{-i\omega a}\hat{f}(\omega)$

Preuve:
$$\begin{align}
    f(x-a) & \leftrightarrow \int{f(x-a)e^{-i\omega x}dx}  \\
    & \leftrightarrow \int{f(u)e^{-iw(u+a)}du} \ \ \ \ u=x-a \\
    & \leftrightarrow \int{f(u)e^{-iwu}e^{-iwa}du} \\
    & \leftrightarrow e^{-iwa} \hat{f}(\omega)
\end{align}$$

3. **Translation fréquentielle**: $f(x)e^{iax} \leftrightarrow \hat{f}(\omega - a)$

Preuve:
$$\begin{align}
    f(x)e^{iax} & \leftrightarrow \int{f(x)e^{ia x}e^{-i\omega x}dx}  \\
     & \leftrightarrow \int{f(x)e^{ia x -i\omega x}dx} \\
     & \leftrightarrow \int{f(x)e^{-ix(\omega -a)}dx} \\
     & \leftrightarrow \hat{f}(\omega - a)
\end{align}$$

4. **Mise à l'échelle**: $f(ax) \leftrightarrow \frac{1}{|a|} \hat{f}\left(\frac{\omega}{a}\right)$

$$\begin{align}
    f(ax) & \leftrightarrow \int{f(ax)e^{-i\omega x}dx} \\
    & \leftrightarrow \frac{1}{a}\int{f(u)e^{-i\frac{\omega}{a} u}du} \ \ \ u=ax \\
    & \leftrightarrow \frac{1}{a} \hat{f}\left(\frac{\omega}{a}\right)

\end{align}$$

5. **Dérivation**: $f^{(k)}(x) \leftrightarrow {(i\omega)}^k\hat{f}(\omega)$

6. **La multiplication dans le domaine fréquentiel**: $f_1(x)*f_2(x)\leftrightarrow \hat{f_1}(\omega)\hat{f_2}(\omega)$

7. **Associativité de la convolution**: $((f*g)*h)(t)=(f*(g*h))(t)$

#### Convolution

Soit des fonctions continues $f(t)$ et $g(t)$. On définit la convolution de $f$ avec $g$, notée $f*g$ comme la fonction
$$ h(x) = (f*g)(x)=\int{f(t)g(x-t)dt}$$


```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.integrate as scpint

t = np.linspace(-5, 5, 1000)
x = np.linspace(-3, 3, 10)

f = np.piecewise(t, [np.abs(t) < 1, np.abs(t) > 1], [1, 0])
g = np.piecewise(t, [np.abs(t) < 2, np.abs(t) > 2], [0.25, 0])

plt.plot(t, f, label=r'$f(t)$')
plt.plot(t, g, label=r'$g(t)$')

plt.legend()
plt.show()

for i in range(x.shape[0]):
    f = np.piecewise(t, [np.abs(t) < 1, np.abs(t) > 1], [1, 0])
    h = np.piecewise(x[i]-t, [np.abs(x[i]-t) < 2, np.abs(x[i]-t) > 2], [0.25, 0])

    plt.plot(t, f, label=r'$f(t)$')
    plt.plot(t, h, label=r'$h(1-t)$')
    plt.plot(t, f * h, label=f'$f(t)h( {round(x[i],2)} - t)$')

    plt.fill_between(t, f * h, color="tomato")
    plt.legend()
    plt.show()

    print(f"Resultat de la convolution pour x = {round(x[i],2)}:",scpint.simpson(f*h,t))

x = np.linspace(-5, 5, 1000)
h = np.zeros_like(x)

for i in range(x.shape[0]):
    g_x = np.piecewise(x[i]-t, [np.abs(x[i]-t) < 2, np.abs(x[i]-t) > 2], [0.25, 0])

    h[i] = scpint.simpson(f * g_x, t)

plt.plot(t, f, label=r'$f(t)$')
plt.plot(t, g, label=r'$g(t)$')
plt.plot(t, h, label=r'$f(t) * g(t)$')

plt.legend()
plt.show()

```


    
![png](Note%20de%20cours_files/Note%20de%20cours_109_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_1.png)
    


    Resultat de la convolution pour x = -3.0: 0.0



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_3.png)
    


    Resultat de la convolution pour x = -2.33: 0.1668335001668335



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_5.png)
    


    Resultat de la convolution pour x = -1.67: 0.3319986653319986



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_7.png)
    


    Resultat de la convolution pour x = -1.0: 0.5005005005005003



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_9.png)
    


    Resultat de la convolution pour x = -0.33: 0.5005005005005003



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_11.png)
    


    Resultat de la convolution pour x = 0.33: 0.5005005005005003



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_13.png)
    


    Resultat de la convolution pour x = 1.0: 0.5005005005005003



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_15.png)
    


    Resultat de la convolution pour x = 1.67: 0.33366700033366686



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_17.png)
    


    Resultat de la convolution pour x = 2.33: 0.16850183516850178



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_19.png)
    


    Resultat de la convolution pour x = 3.0: 0.0



    
![png](Note%20de%20cours_files/Note%20de%20cours_109_21.png)
    


On peut ajouter une autre propriété de la transformée de Fourier:

**La multiplication dans le domaine fréquentiel**: $f_1(x)*f_2(x)\leftrightarrow \hat{f_1}(\omega)\hat{f_2}(\omega)$

La plupart des opérations peuvent être réécrites comme des convolutions pour faire un gain de performance

# Cours 14

### Chapitre 7: Transformée de Fourier discrète

#### Définition: 
Elle permet de prendre n'importe quelle fonction discrète et de l'amener dans le domaine fréquentiel. 
Souvent représentée par l'acronyme *DFT*

Si on a $f = [f_0, f_1, f_n]$ alors $\hat{f} = [\hat{f}_0,\hat{f}_1,\hat{f}_n]$ où:
$$\hat{f}_k = \sum^n_{j=0}{f_je^{\frac{-i2\pi jk}{n}}}$$

On a également que:
$$ f_k = \frac{1}{n+1}\sum^n_{j=0}{\hat{f}_je^{\frac{i2\pi jk}{n}}}$$
est la transformée de Fourier discrète inverse.

#### Transformée de Fourier rapide
Souvent représentée par l'acronyme *FFT*
Beaucoup plus efficace que la DFT

**Puisqu'on utilise toujours des fonctions réelles dans le cours, on peut utiliser les fonctions:**
```python
rfft()
irfft()
```

Pour transformer notre axe de *numéro de fréquence* en Hz, *SciPy* propose la fonction suivante:
```python
rfftfreq()
```


#### Exemples d'utilisation:

##### Manipulation fréquentielle de base:
On veut retirer la fréquence de 120Hz

La règle pour trouver la position:

position $ = $ fréquence $ \times dt \times n$


```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.fft as scpfft

t = np.linspace(0, 0.25, 1000)
f = np.sin(2*np.pi*50*t) + np.sin(2*np.pi*120*t)

plt.plot(t, f)
plt.title('Signal original')
plt.show()

F = scpfft.rfft(f)

dt = 0.25 / t.shape[0]
freq = scpfft.rfftfreq(t.shape[0], dt)

plt.plot(freq, np.abs(F))
plt.title('Spectre d\'amplitude original (Hz)')
plt.show()

position120 = int(120 * dt * t.shape[0])
F[position120-2:position120+3] = 0

plt.plot(freq, np.abs(F))
plt.title('Spectre d\'amplitude modifié (Hz)')
plt.show()

f2 = scpfft.irfft(F)

plt.plot(t, f2.real)
plt.title('Signal reconstruit')
plt.show()


```


    
![png](Note%20de%20cours_files/Note%20de%20cours_113_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_113_1.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_113_2.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_113_3.png)
    


##### Débruitage d'une fonction


```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.fft as scpfft

file = open('dataset/f_bruit.txt', 'r')
f = file.read().removeprefix("f_bruit = [").removesuffix("]").replace('\n', '').split(', ')

data = np.array(f, dtype = float)

plt.plot(data)
plt.title('Signal original')
plt.show()

F = scpfft.rfft(data)


plt.plot(np.abs(F))
plt.title('Spectre d\'amplitude original (Hz)')
plt.show()

seuil = 200

for i in range(F.shape[0]):
    if np.abs(F[i]) < seuil: 
        F[i] = 0

plt.plot(freq, np.abs(F))
plt.title('Spectre d\'amplitude modifié (Hz)')
plt.show()

f2 = scpfft.irfft(F)

plt.plot(f2.real)
plt.title('Signal modifié reconstruit')
plt.show()

```


    
![png](Note%20de%20cours_files/Note%20de%20cours_115_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_115_1.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_115_2.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_115_3.png)
    


# Cours 15

##### Fonctionnement de Shazam

On combine le temps et les fréquences pour obtenir un spectrogramme

Python permet la création d'un spectrogramme avec la library
```python
import scipy.signal as scpsig
scpsig.spectrogram()
```
### Transformée de Fourier discrète à deux dimensions
#### Définition et calcul
Si on a un tableau $n \times m$, on calcule la transformée de Fourier sur chaque ligne et ensuite on évalue la transformée de Fourier sur chaque colonne du résultat de l'opération précédente.


```python
import numpy as np
import skimage as ski
import scipy.fft as scpfft
import matplotlib.pyplot as plt

img = ski.io.imread("dataset/corgis.png")

img_freq = scpfft.fft2(img)

img_freq_shift = scpfft.fftshift(img_freq)

ski.io.imshow(255*np.log(1+np.abs(img_freq_shift)), cmap="gray")
ski.io.show()

img_out = scpfft.ifft2(img_freq)

ski.io.imshow(img_out.real, cmap="gray")
ski.io.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_117_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_117_1.png)
    


Quelques exemples de transformée de Fourier sur une image


```python
import numpy as np
import scipy.fft as scpfft
import matplotlib.pyplot as plt

img_carre = np.zeros((501, 501))
img_carre[240:261, 240:261] = 255
plt.imshow(img_carre, cmap = 'gray')
plt.axis('off')
plt.show()

img_carre_freq = scpfft.fft2(img_carre)
img_carre_freq_shift = scpfft.fftshift(img_carre_freq)
plt.imshow(255*np.log(1+np.abs(img_carre_freq_shift)), cmap = 'gray')
plt.axis('off')
plt.show()

img_carre_shift = np.zeros((501, 501))
img_carre_shift[140:161, 140:161] = 255
plt.imshow(img_carre_shift, cmap = 'gray')
plt.axis('off')
plt.show()

img_carre_shift_freq = scpfft.fft2(img_carre_shift)
img_carre_shift_freq_shift = scpfft.fftshift(img_carre_shift_freq)
plt.imshow(255*np.log(1+np.abs(img_carre_shift_freq_shift)), cmap = 'gray')
plt.axis('off')
plt.show()

img_rect = np.zeros((501, 501))
img_rect[230:271, 240:261] = 255
plt.imshow(img_rect, cmap = 'gray')
plt.axis('off')
plt.show()

img_rect_freq = scpfft.fft2(img_rect)
img_rect_freq_shift = scpfft.fftshift(img_rect_freq)
plt.imshow(255*np.log(1+np.abs(img_rect_freq_shift)), cmap = 'gray')
plt.axis('off')
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_119_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_119_1.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_119_2.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_119_3.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_119_4.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_119_5.png)
    


# Cours 16

#### Application à la compression d'images
On cherche à réduire de 90% la taille d'un fichier.

Une **mauvaise** idée serait de s'attaquer aux pixels de l'image: en diminuant leur quantité ou en réduisant leur capacité de représentation des couleurs.


```python
import numpy as np
import skimage as ski
import matplotlib.pyplot as plt

img = ski.io.imread("dataset/fatbike.png")
plt.imshow(img, cmap = 'gray')
plt.axis('off')
plt.show()

# Mauvaise idée: conserver seulement 1 pixel sur 10
small_img = img[::10, ::10]
plt.imshow(small_img, cmap = 'gray')
plt.axis('off')
plt.show()

# Mauvaise idée 2.0: réduire la capacité de stockage de couleur de chaque pixel
small_img = np.zeros_like(img)
for i in range(small_img.shape[0]):
    for j in range(small_img.shape[1]):
        small_img[i, j] = 25 * round(img[i, j] / 25)
plt.imshow(small_img, cmap = 'gray')
plt.axis('off')
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_121_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_121_1.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_121_2.png)
    


On devrait plutôt s'attaquer à la représentation fréquentielle de l'image

On va éliminer les fréquences ayant les plus petites amplitudes et on va les éliminer. On va seulement préserver les fréquences dans les $10\%$ les plus fréquentes.


```python
from turtle import position
import numpy as np
import skimage as ski
import matplotlib.pyplot as plt
import scipy.fft as scpfft

img = ski.io.imread("dataset/fatbike.png")
plt.imshow(img, cmap = 'gray')
plt.axis('off')
plt.show()

img_freq = scpfft.fft2(img)

img_freq_line = img_freq.reshape(-1)
img_freq_line = np.abs(img_freq_line)
img_freq_line.sort()

position = int(0.9 * img_freq_line.shape[0])
valeur = img_freq_line[position]

img_freq_comp = img_freq.copy()

img_freq_comp[np.abs(img_freq) < valeur] = 0

img_out = scpfft.ifft2(img_freq_comp)
plt.imshow(np.abs(img_out), cmap = 'gray')
plt.axis('off')
plt.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_123_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_123_1.png)
    


### Convolution

Si on a deux fonctions discrètes: on peut calculer la convolution de $f$ et $g$ comme:
$$h_n=\sum^\infty_{k=-\infty}{f_kg_{n-k}}$$

Dans la library scipy, on peut utiliser la fonction:
```python
from scipy.signal import convolve, fftconvolve
convolve()
fftconvolve()
```


```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import fftconvolve

data = np.genfromtxt('dataset/elevation.txt')

m = 51

filt = np.ones((1,m)) / m
filt = filt.reshape(-1)

data_filt = fftconvolve(data, filt, mode = 'valid')

plt.plot(data, label = 'Altitude')
plt.title('Altitude (m) en fonction du temps (s)')
plt.show()

plt.plot(data_filt, label = 'Altitude filtrée')
plt.title('Altitude (m) filtrée en fonction du temps (s)')
plt.show()



```


    
![png](Note%20de%20cours_files/Note%20de%20cours_125_0.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_125_1.png)
    


Si on a des fonctions deux dimensions:
$$h_{i,j}=\sum^\infty_{s=-\infty}{\sum^\infty_{t=-\infty}{f_{i,j}g_{i-s,j-t}}}$$



```python
import numpy as np
import matplotlib.pyplot as plt
import skimage.io as ski
from scipy.signal import fftconvolve, convolve
import scipy.fft as scpfft
import time

img = ski.imread('dataset/fatbike.png')

plt.imshow(img, cmap = 'gray')
plt.axis('off')
plt.show()

startTime = time.time()
m = 3
img_filt3 = np.zeros_like(img)
for i in range(img.shape[0]):
        for j in range(img.shape[1]):
            debut_i = max(0, i - m)
            fin_i = min(img.shape[0]-1, i + m)
            debut_j = max(0, j - m)
            fin_j = min(img.shape[1]-1, j + m)
            img_filt3[i, j] = np.mean(img[debut_i:fin_i+1, debut_j:fin_j+1])

m = 7
endTime = time.time()
print("Temps d'exécution boucle:", endTime - startTime)

filt = np.ones((m, m)) / m**2

startTime = time.time()
# Équivalent à tout ce qu'il y a en haut
img_filt4 = convolve(img, filt, mode = 'valid', method='direct')
endTime = time.time()

print("Temps d'exécution convolve():", endTime - startTime)

startTime = time.time()
img_freq = scpfft.fft2(img)
filt_freq = scpfft.fft2(filt, s = img.shape)

img_filt_freq = img_freq * filt_freq
img_filt = scpfft.ifft2(img_filt_freq).real

endTime = time.time()
print("Temps d'exécution convolution à la main:", endTime - startTime)

startTime = time.time()
# Équivalent à tout ce qu'il y a en haut
img_filt2 = fftconvolve(img, filt, mode = 'valid')
endTime = time.time()

print("Temps d'exécution fftconvolve():", endTime - startTime)


plt.imshow(img_filt, cmap = 'gray')
plt.axis('off')
plt.show()

```


    
![png](Note%20de%20cours_files/Note%20de%20cours_127_0.png)
    


    Temps d'exécution boucle: 3.4189398288726807
    Temps d'exécution convolve(): 0.506087064743042
    Temps d'exécution convolution à la main: 0.03545498847961426
    Temps d'exécution fftconvolve(): 0.02142190933227539



    
![png](Note%20de%20cours_files/Note%20de%20cours_127_2.png)
    


# Cours 17

### Chapitre 8: Échantillonnage et quantification

Pour passer d'une représentation annalogue à une représentation numérique, il faut faire deus opérations:
* Quantifier veut dire limiter la précision d'une mesure
* Échantillonner veut dire limiter le nombre de donnée sur un intervalle de temps

#### Quantification

On assigne les valeurs maximales et minimales à un ensemble de valeurs préétablises. Cette ensemble comportera un certain nombre de **bits**. Une quantification de $k$ bits permettra $2^k$ valeur entre $v_{min}$ et $v_{max}$. On a donc:
$$\Delta v = \frac{v_{max}-v_{min}}{2^k}$$

La différence entre le signal original et le signal quantifié est le **bruit de quantification**



# Cours 18

#### Échantillonnage
##### Principe de fonctionnement
Si on a une fonction continue et $T$ l'intervalle de temps entre deux valeurs de $t$ qu'on souhaite conserver. On obtiendra alors la séquence de valeurs définies par $S_i=S(nT)$ où $n$ est un nombre entier. La **fréquence d'échantillonnage** est alors $f_s=\frac{1}{T}$.

Comment déterminer la fréquence d'échantillonnage:

**Le théorème de Nyquist-Shannon:**
Il faut que la fréquence d'échantillonnage soit au moins le double de la fréquence maximale dans un signal.

Réciproquement, l'échantillonnage avec des échantillons régulièrement espacés peut parfaitement décrire un signal à condition qu'il ne contienne aucune fréquence supérieur à la moitié de la fréquence d'échantillonnage, dite fréquence de Nyquist.
##### Crénelage (aliasing)
S'il y a des fréquences supérieures à la fréquence de Nyquist, il y aura du crénelage aussi appelé repliement spectral

**Pour prédire le repliement spectral:**

La fréquence de Nyquist fait office d'axe de réflexion pour toutes les autres fréquences

##### Échantillonnage visuel
Lorsqu'il n'y a pas assez de pixel pour représenter les variations de hautes fréquences.


# Devoirs:

### Devoir 1


```python
import numpy as np
import skimage.io as ski
import matplotlib.pyplot as plt

def gradient_image(img):
    G = np.zeros((img.shape[0], img.shape[1], 2))

    # Ajouter du code ici
    ddx = np.gradient(img, axis = 1)
    ddy = np.gradient(img, axis = 0)
    G[:, :, 0] = ddx
    G[:, :, 1] = ddy

    return G

def norme_gradient(grad):
    N = np.zeros(grad.shape[0:2])

    # Ajouter du code ici
    N = np.sqrt(grad[:,:,0]**2 + grad[:,:,1]**2)

    return N

def image_contour(N, s):
    C = np.zeros_like(N)

    # Ajouter du code ici
    C = N > s

    return C * 255

def moyenne_image(img, m):
    Im = np.zeros_like(img)

    # Ajouter du code ici
    for i in range(img.shape[0]):
        for j in range(img.shape[1]):
            debuti = max(0, i - m)
            fini = min(img.shape[0]-1, i + m)
            debutj = max(0, j - m)
            finj = min(img.shape[1]-1, j + m)
            Im[i, j] = np.mean(img[debuti:fini+1, debutj:finj+1])
    

    return Im

def mediane_image(img, m):
    Im = np.zeros_like(img)

    # Ajouter du code ici
    for i in range(img.shape[0]):
        for j in range(img.shape[1]):
            debuti = max(0, i - m)
            fini = min(img.shape[0]-1, i + m)
            debutj = max(0, j - m)
            finj = min(img.shape[1]-1, j + m)
            Im[i, j] = np.median(img[debuti:fini+1, debutj:finj+1])

    return Im

image = ski.imread("dataset/fatbike.png")
ski.imshow(image)
ski.show()

# Paramètres
moyenne_m = 3
mediane_m = 3
seuil_s = 15

# Détection de contours sur l'image originale

print("Calcul du gradient...")
G = gradient_image(image)

ski.imshow(G[:,:,0].astype(np.uint8) + 128, cmap=plt.cm.gray)
ski.show()
ski.imshow(G[:,:,1].astype(np.uint8) + 128, cmap=plt.cm.gray)
ski.show()

print("Calcul de la norme du gradient...")
N = norme_gradient(G)

ski.imshow((255*N[:,:]/N.max()).astype(np.uint8), cmap=plt.cm.gray)
ski.show()

print("Application du seuil...")
C = image_contour(N, seuil_s)

ski.imshow(C.astype(np.uint8), cmap=plt.cm.gray)
ski.show()

# Détection de contours sur l'image moyenne

print("Calcul de l'image moyenne...")
image_moy = moyenne_image(image, moyenne_m)

ski.imshow(image_moy.astype(np.uint8), cmap=plt.cm.gray)
ski.show()

print("Calcul du gradient...")
G = gradient_image(image_moy)

ski.imshow(G[:,:,0].astype(np.uint8) + 128, cmap=plt.cm.gray)
ski.show()
ski.imshow(G[:,:,1].astype(np.uint8) + 128, cmap=plt.cm.gray)
ski.show()

print("Calcul de la norme du gradient...")
N = norme_gradient(G)

ski.imshow((255*N[:,:]/N.max()).astype(np.uint8), cmap=plt.cm.gray)
ski.show()

print("Application du seuil...")
C = image_contour(N, seuil_s)

ski.imshow(C.astype(np.uint8), cmap=plt.cm.gray)
ski.show()

# Détection de contours sur l'image médiane

print("Calcul de l'image médiane...")
image_med = mediane_image(image, mediane_m)

ski.imshow(image_moy.astype(np.uint8), cmap=plt.cm.gray)
ski.show()

print("Calcul du gradient...")
G = gradient_image(image_med)

ski.imshow(G[:,:,0].astype(np.uint8) + 128, cmap=plt.cm.gray)
ski.show()
ski.imshow(G[:,:,1].astype(np.uint8) + 128, cmap=plt.cm.gray)
ski.show()

print("Calcul de la norme du gradient...")
N = norme_gradient(G)

ski.imshow((255*N[:,:]/N.max()).astype(np.uint8), cmap=plt.cm.gray)
ski.show()

print("Application du seuil...")
C = image_contour(N, seuil_s)

ski.imshow(C.astype(np.uint8), cmap=plt.cm.gray)
ski.show()
```


    
![png](Note%20de%20cours_files/Note%20de%20cours_131_0.png)
    


    Calcul du gradient...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_2.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_3.png)
    


    Calcul de la norme du gradient...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_5.png)
    


    Application du seuil...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_7.png)
    


    Calcul de l'image moyenne...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_9.png)
    


    Calcul du gradient...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_11.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_12.png)
    


    Calcul de la norme du gradient...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_14.png)
    


    Application du seuil...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_16.png)
    


    Calcul de l'image médiane...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_18.png)
    


    Calcul du gradient...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_20.png)
    



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_21.png)
    


    Calcul de la norme du gradient...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_23.png)
    


    Application du seuil...



    
![png](Note%20de%20cours_files/Note%20de%20cours_131_25.png)
    


### Devoir 2


```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm

def simpson(f, a, b, n) :

    # INSCRIRE DU CODE ICI
    x = np.linspace(a, b, 2*n+1)
    y = f(x)
    dx = (b - a) / n

    integrale = (dx/6) * np.sum(
        y[:-1:2] + # Sélectionne les éléments d'indice pair sauf le dernier (Points à gauche de l'intervalle)
        4*y[1::2] + # Sélectionne les éléments d'indice impair (Points au milieu de l'intervalle)
        y[2::2] # Sélectionne les éléments d'indice pair sauf le premier (Points à droite de l'intervalle)
            )
    
    return integrale

# Fonction récursive pour calculer la dérivée d'ordre n
def derivee(y, x, ordre=1):
    dydx = np.gradient(y, x)

    if ordre > 1:
        dydx = derivee(dydx, x, ordre-1)
    return dydx

# Fonction pour calculer le nombre d'intervalles nécessaires pour une certaine erreur maximale
def nbIntervallesPourErreurMaximale(f, a, b, erreur_maximale):
    x = np.linspace(a, b, 1000)
    y = f(x)
    val_max_dev_4 = np.max(np.abs(derivee(y, x, 4)))
    intervalles = (( ((b - a) ** 5) / (180 * erreur_maximale) ) * val_max_dev_4) ** (1/4)
    return int(np.ceil(intervalles))

# Spécifier la moyenne et l'écart type de la loi normale
mu = float(input("Moyenne de la loi normale : "))
sigma = float(input("Écart type de la loi normale : "))

# Définition de la fonction normale à partir de mu et sigma

# INSCRIRE DU CODE ICI
# Vous devez changer la fonction pour celle décrivant une loi normale de moyenne mu et d'écart type sigma
f = lambda x : norm.pdf(x, loc=mu, scale=sigma)

# Graphique de la courbe associée à la loi normale
x = np.linspace(mu-4 * sigma, mu+4 * sigma, 1000)
y = f(x)
ax = plt.subplot(111)
ax.plot(x, y, label="N(%.2f, %.2f)" % (mu, sigma**2), color='dodgerblue')
box = ax.get_position()
ax.set_position([box.x0, box.y0 + box.height * 0.1, box.width, box.height * 0.9])

# Spécifier le type de probabilité à évaluer
print("Quel type de probabilité voulez-vous évaluer ?")
print("\t \t 1. P(X < a)")
print("\t \t 2. P(a < X < b)")
print("\t \t 3. P(X > a)")
type_probabilite = int(input("Type de probabilité : "))
while type_probabilite not in {1, 2, 3}:
    type_probabilite = int(input("Choisir le type 1, 2 ou 3 : "))

erreur_maximale = 0.001

if type_probabilite == 1:
    a = float(input("Valeur du a dans P(X < a) : "))

    # Évaluation de la probabilité
    if a < mu:
        p = 0
        # Calcul du nombre de sous intervalles nécessaire

        # INSCRIRE DU CODE ICI
        n = nbIntervallesPourErreurMaximale(f, a, mu, erreur_maximale)
        # Évaluation de la probabilité
        
        # INSCRIRE DU CODE ICI
        p = 0.5 - simpson(f, a, mu, n)
    else:
        p = 0
        # Calcul du nombre de sous intervalles nécessaire

        # INSCRIRE DU CODE ICI
        n = nbIntervallesPourErreurMaximale(f, mu, a, erreur_maximale)
        
        # Évaluation de la probabilité
        
        # INSCRIRE DU CODE ICI
        p = 0.5 + simpson(f, mu, a, n)

    print("La probabilité P(X < %.3f) vaut %.6f" % (a, p))

    # Tracer la région associée à la probabilité
    x_prob = np.linspace(mu-4 * sigma, a, 100)
    y_prob = f(x_prob)
    plt.vlines(a, ymin=0, ymax=f(a), color='dodgerblue')
    plt.fill_between(x_prob, y_prob, color='skyblue', label="P(X < %.3f) = %.6f" % (a, p)) # type: ignore
    plt.title("Loi normale de moyenne %.2f et d\'écart type %.2f" % (mu, sigma))
    ax.legend(loc='upper center', bbox_to_anchor=(0.5, -0.075))

elif type_probabilite == 2:
    a = float(input("Valeur du a dans P(a < X < b) : "))
    b = float(input("Valeur du b dans P(a < X < b) : "))
    while b < a:
        print("Il faut que a soit inférieur à b.")
        a = float(input("Valeur du a dans P(a < X < b) : "))
        b = float(input("Valeur du b dans P(a < X < b) : "))

    p = 0
    # Calcul du nombre de sous intervalles nécessaire

    # INSCRIRE DU CODE ICI
    n = nbIntervallesPourErreurMaximale(f, a, b, erreur_maximale)

    # Évaluation de la probabilité
    
    # INSCRIRE DU CODE ICI
    p = simpson(f, a, b, n)
    print("La probabilité P(%.3f < X < %.3f) vaut %.6f" % (a, b, p))

    # Tracer la région associée à la probabilité
    x_prob = np.linspace(a, b, 100)
    y_prob = f(x_prob)
    plt.vlines(a, ymin=0, ymax=f(a), color='dodgerblue')
    plt.vlines(b, ymin=0, ymax=f(b), color='dodgerblue')
    plt.fill_between(x_prob, y_prob, color='skyblue', label="P(%.3f < X < %.3f) = %.6f" % (a, b, p)) # type: ignore
    plt.title("Loi normale de moyenne %.2f et d\'écart type %.2f" % (mu, sigma))
    ax.legend(loc='upper center', bbox_to_anchor=(0.5, -0.075))

elif type_probabilite == 3:
    a = float(input("Valeur du a dans P(X > a) : "))
    # Évaluation de la probabilité
    if a < mu:
        p = 0
        # Calcul du nombre de sous intervalles nécessaire

        # INSCRIRE DU CODE ICI
        n = nbIntervallesPourErreurMaximale(f, a, mu, erreur_maximale)

        # Évaluation de la probabilité
        
        # INSCRIRE DU CODE ICI
        p = 0.5 + simpson(f, a, mu, n)
    else:
        p = 0
        # Calcul du nombre de sous intervalles nécessaire

        # INSCRIRE DU CODE ICI
        n = nbIntervallesPourErreurMaximale(f, mu, a, erreur_maximale)

        # Évaluation de la probabilité
        
        # INSCRIRE DU CODE ICI
        p = 0.5 - simpson(f, mu, a, n)

    print("La probabilité P(X > %.3f) vaut %.6f" % (a, p))

    # Tracer la région associée à la probabilité
    x_prob = np.linspace(a, mu+4*sigma, 100)
    y_prob = f(x_prob)
    plt.vlines(a, ymin=0, ymax=f(a), color='dodgerblue')
    plt.fill_between(x_prob, y_prob, color='skyblue', label="P(X > %.3f) = %.6f" % (a, p)) # type: ignore
    plt.title("Loi normale de moyenne %.2f et d\'écart type %.2f" % (mu, sigma))
    ax.legend(loc='upper center', bbox_to_anchor=(0.5, -0.075))

plt.show()

```

    Quel type de probabilité voulez-vous évaluer ?
    	 	 1. P(X < a)
    	 	 2. P(a < X < b)
    	 	 3. P(X > a)
    La probabilité P(-0.500 < X < 0.500) vaut 0.382925



    
![png](Note%20de%20cours_files/Note%20de%20cours_133_1.png)
    


### Devoir 3


```python
import numpy as np
from numpy.linalg import norm
from scipy.io import wavfile
from scipy.fft import rfft
import pygame
import sys

# Ouverture du fichier musical pour l'analyse
fs, data = wavfile.read("dataset/audio/sweep3.wav")

# Séparation des canaux gauche-droite
data_left = data[:, 0] / 2 ** 15
data_right = data[:, 1] / 2 ** 15

# Initialisation de la fenêtre graphique
pygame.init()
display = (800, 600)
surface = pygame.display.set_mode(display)

# Ouverture du fichier musical pour la lecture
pygame.mixer.music.load("dataset/audio/sweep3.wav")
pygame.mixer.music.play(0)
# pygame.mixer.music.set_volume(0.5)
play_time = pygame.time.get_ticks()

color_temporelle = (40, 204, 237)
color_freq = (237, 40, 237)

t = pygame.time.get_ticks()
getTicksLastFrame = t

# Paramètres pour la visualisation temporelle
current_height_left = 0
current_height_right = 0

# Paramètres pour la visualisation fréquentielle
nb_columns = 30
deltaFreq = int(6000 / nb_columns)
bars_top = np.zeros((nb_columns, 1))
bars_top_old = bars_top

# Dernière touche appuyée sur le clavier (t = analyse temporelle, f = analyse fréquentielle, q = quitter)
last_key = pygame.K_t

# Boucle principale
while True:
    # Interaction avec le clavier
    events = pygame.event.get()
    for event in events:
        if event.type == pygame.QUIT:
            pygame.display.quit()
            pygame.quit()
            sys.exit()
        elif event.type == pygame.KEYDOWN:
            if event.key == pygame.K_q:
                pygame.display.quit()
                pygame.quit()
                sys.exit()
            elif event.key == pygame.K_t:
                print("Analyse temporelle")
                last_key = pygame.K_t
            elif event.key == pygame.K_f:
                print("Analyse fréquentielle")
                last_key = pygame.K_f

    # Fond noir
    surface.fill((0, 0, 0))

    # Dernière touche = t -> Analyse temporelle
    if last_key == pygame.K_t:
        # Gestion du temps pour garder l'affichage synchronisé avec la musique
        # "t" est le temps actuel
        t = pygame.time.get_ticks() - play_time
        deltaTime = (t - getTicksLastFrame) / 1000.0
        getTicksLastFrame = t

        # AJOUTER DU CODE ICI
        # chunk_left et chunk_right sont des tableaux contenant les données temporelles à analyser
        # l'intervalle d'analyse contient les valeurs entre t - 0,01s et t + 0,01s

        position = int(t * fs / 1000)
        delta_position = int(0.01 * fs)

        debut = max(0, position - delta_position)
        fin_left = min(data_left.shape[0] - 1, position + delta_position)
        fin_right = min(data_right.shape[0] - 1, position + delta_position)

        chunk_left = data_left[debut:fin_left]
        chunk_right = data_right[debut:fin_right]

        # AJOUTER DU CODE ICI
        # norm_left et norm_right correspondent à la racine carrée de la somme des carrés des éléments
        # de chunk_left et chunk_right, respectivement
        norm_left = norm(chunk_left)
        norm_right = norm(chunk_right)

        # Gauche
        desired_height_left = 30 * norm_left
        speed = (desired_height_left - current_height_left) / 0.1
        new_height_left = current_height_left + speed * deltaTime
        current_height_left = new_height_left

        # Droit
        desired_height_right = 30 * norm_right
        speed = (desired_height_right - current_height_right) / 0.1
        new_height_right = current_height_right + speed * deltaTime
        current_height_right = new_height_right

        # Construction des colonnes
        points = [(200, 500),
                  (200, 500-new_height_left),
                  (300, 500-new_height_left),
                  (300, 500),
                  (500, 500),
                  (500, 500-new_height_right),
                  (600, 500-new_height_right),
                  (600, 500)]

        # Affichage
        pygame.draw.polygon(surface, color_temporelle, points)

    elif last_key == pygame.K_f:
        # Gestion du temps pour garder l'affichage synchronisé avec la musique
        # "t" est le temps actuel
        t = pygame.time.get_ticks() - play_time
        deltaTime = (t - getTicksLastFrame) / 1000.0
        getTicksLastFrame = t

        # AJOUTER DU CODE ICI
        # chunk_left et chunk_right sont des tableaux contenant les données temporelles à analyser
        # l'intervalle d'analyse contient les valeurs entre t - 0,25s et t + 0,25s
        position = int(t * fs / 1000)
        delta_position = int(0.25 * fs)

        debut = max(0, position - delta_position)
        fin_left = min(data_left.shape[0] - 1, position + delta_position)
        fin_right = min(data_right.shape[0] - 1, position + delta_position)
        chunk_left = data_left[debut:fin_left]
        chunk_right = data_right[debut:fin_right]

        # AJOUTER DU CODE ICI
        # chunk_left_hat et chunk_right_hat sont les transformées de Fourier de chunk_left et chunk_right, resp.
        chunk_left_hat = rfft(chunk_left)
        chunk_right_hat = rfft(chunk_right)

        # AJOUTER DU CODE ICI
        # chunk_amp est la moyenne des spectres amplitudes de chunk_left_hat et chunk_right_hat
        chunk_amp = np.mean([np.abs(chunk_left_hat), np.abs(chunk_right_hat)], axis=0) # TODO: vérifier si c'est bien l'amplitude

        # AJOUTER DU CODE ICI
        # deltaPosition représente l'écart "en position" entre le début et la fin des fréquences
        # associées à une colonne en fonction de l'écart "en fréquence" deltaFreq
        deltaPosition = int(deltaFreq * (1/fs) * chunk_amp.shape[0])

        # Construction des colonnes
        points = [(25, 500)]
        for i in range(nb_columns):
            # AJOUTER DU CODE ICI
            # amp représente la moyenne des amplitudes des fréquences associées à la i-ième colonne
            amp = np.mean(chunk_amp[i*deltaPosition:(i+1)*deltaPosition])

            # Conversion des amplitudes en décibels
            amp_db = np.clip(20 * np.log10(amp / 32768), -80, 0) + 80
            current_height = bars_top_old[i]
            desired_height = 5 * amp_db
            speed = (desired_height - current_height) / 0.04
            bars_top[i] = current_height + speed * deltaTime
            points.append((25 + i * 25, 500 - bars_top[i, 0]))
            points.append((25 + (i + 1) * 25, 500 - bars_top[i, 0]))
        points.append((775, 500))

        # Affichage
        pygame.draw.polygon(surface, color_freq, points)

    # Rafraichissement
    pygame.display.flip()

```

    pygame 2.5.2 (SDL 2.28.3, Python 3.11.5)
    Hello from the pygame community. https://www.pygame.org/contribute.html



    An exception has occurred, use %tb to see the full traceback.


    SystemExit



    /Users/zacharieroy/anaconda3/lib/python3.11/site-packages/IPython/core/interactiveshell.py:3534: UserWarning: To exit: use 'exit', 'quit', or Ctrl-D.
      warn("To exit: use 'exit', 'quit', or Ctrl-D.", stacklevel=1)


### Autopilot


```python
import numpy as np
import skimage as ski
import skvideo.io
import matplotlib.pyplot as plt
import cv2 as cv
from scipy.stats import norm
from scipy.signal import fftconvolve

np.float = np.float64
np.int = np.int_

def gradient_image(img):
    G = np.zeros((img.shape[0], img.shape[1], 2))
    
    # Méthode avec Sobel filters
    kernel_x = np.array([-1, 0, 1](-1,%200,%201))
    kernel_y = np.array([1, 2, 1](1,%202,%201))
    G[:,:,0] = fftconvolve(img, kernel_x, mode='same')
    G[:,:,1] = fftconvolve(img, kernel_y, mode='same')

    N = np.hypot(G[:,:,0], G[:,:,1])
    N = N / N.max() * 255
    theta = np.arctan2(G[:,:,1], G[:,:,0])
    return N, theta

def non_maximum_suppression(G, theta):
    M, N = G.shape
    Z = np.zeros((M,N), dtype=np.int32)
    angle = theta * 180. / np.pi
    angle[angle < 0] += 180

    for i in range(1, M-1):
        for j in range(1, N-1):
            
            q = 255
            r = 255

            # Split en 8 directions
            if (0 <= angle[i,j] < 22.5) or (157.5 <= angle[i,j] <= 180):
                q = G[i, j+1]
                r = G[i, j-1]
            elif (22.5 <= angle[i,j] < 67.5):
                q = G[i+1, j-1]
                r = G[i-1, j+1]
            elif (67.5 <= angle[i,j] < 112.5):
                q = G[i+1, j]
                r = G[i-1, j]
            elif (112.5 <= angle[i,j] < 157.5):
                q = G[i-1, j-1]
                r = G[i+1, j+1]
            
            if (G[i,j] >= q) and (G[i,j] >= r):
                Z[i,j] = G[i,j]
            else:
                Z[i,j] = 0
    return Z

def hysteresis_double_thresholding(img, T1, T2):
    M, N = img.shape
    resulant = np.zeros((M,N), dtype=np.int32)

    fort = np.int32(255)
    faible = np.int32(25)

    fort_i, fort_j = np.where(img >= T2)
    faible_i, faible_j = np.where((img <= T2) & (img >= T1))

    resulant[fort_i, fort_j] = fort
    resulant[faible_i, faible_j] = faible

    for i in range(1, M-1):
        for j in range(1, N-1):
            if resulant[i,j] == faible:
                if ((resulant[i+1, j-1] == fort) or (resulant[i+1, j] == fort) or (resulant[i+1, j+1] == fort)
                    or (resulant[i, j-1] == fort) or (resulant[i, j+1] == fort)
                    or (resulant[i-1, j-1] == fort) or (resulant[i-1, j] == fort) or (resulant[i-1, j+1] == fort)
                    ):
                    resulant[i, j] = fort
                else:
                    resulant[i, j] = 0

    return resulant

def gaussian_kernel(size, sigma=1):
    kernel_1D = np.linspace(-(size // 2), size // 2, size)
    for i in range(size):
        kernel_1D[i] = norm.pdf(kernel_1D[i], loc=0, scale=sigma)
    kernel_2D = np.outer(kernel_1D.T, kernel_1D.T)
 
    kernel_2D *= 1.0 / kernel_2D.max()

    return kernel_2D

def gaussian_blur(image, kernel_size):
    kernel = gaussian_kernel(kernel_size, sigma=np.sqrt(kernel_size))
    return fftconvolve(image, kernel, mode='same')

def region(image, polygon):

    mask = np.zeros_like(image)

    mask = cv.fillPoly(mask, polygon, 255)
    mask = cv.bitwise_and(image, mask)
    return mask

xleft = np.linspace(300, 600, 1000)
yleft = xleft
xright = np.linspace(680, 980, 1000)
yright = xright

# Chargement de la vidéo en mémoire
video = skvideo.io.vread("dataset/autopilot/stecatherine.mp4", as_grey=True)

# Traitement de chaque image composant la vidéo
for it in range(400, 500):
    fr = video[it,:,:,:]
    img = np.array(fr[:,:,0])

    
    
    # Affichage du numéro l'image traitée
    print(it)
    polygon1 = np.array([
                        [(100, 900), (100, 500), (1280, 500), (1280, 900)]
                        ])
    # Application d'un masque pour réduire le temps de compilation
    img_crop = region(img, polygon1)
    # Application d'un filtre gaussian pour réduire le bruit
    gaussian = gaussian_blur(img_crop, 10)
    # Calcul du module du gradient et de sa norme
    grad, theta = gradient_image(gaussian)
    # Suppression des non-maxima locaux
    max = non_maximum_suppression(grad, theta)
    # Détection des contours avec un double seuil
    contour = hysteresis_double_thresholding(max, 9, 15)

    polygon2 = np.array([
                        [(150, 750), (500, 520), (660, 500), (1000, 700), (1280, 800)]
                        ])
    # Application d'un masque pour ne garder que les lignes de la route dans la région voulue
    C = region(contour, polygon2)

    mask = C

    # Pour débugger, décommentez les lignes suivantes
    # B = np.copy(contour)
    # mask = cv.fillPoly(B, polygon2, 255)

    """

    Pourquoi mon code produit-il un meilleur résultat que la référence?
    
    1. J'ai utilisé un premier masque pour réduire le temps de compilation
    2. J'ai utilisé un filtre gaussien pour réduire le bruit au lieu d'un filtre moyenneur ce qui a permis de mieux détecter les lignes
    3. J'ai implémemté l'agorithme de détection de contour Canny qui implique les étapes suivantes:
        - Calcul du gradient de l'image
            - Utilise la convolution avec un filtre Sobel pour calculer le gradient de l'image réduisant le temps de calcul
        - Suppression des non-maxima locaux
            - Cette étape permet de réduire le nombre de points de contours en ne gardant que les points de contours les plus forts créant un coutour plus précis
        - Détection des contours avec un double seuil
            - Cette étape permet de ne garder que les points de contours les plus forts et d'éliminer les points de contours isolés des autres réduisant ainsi le bruit
    4. J'ai utilisé un deuxième masque pour ne garder que les lignes de la route dans la région voulue éliminant ainsi les lignes parasites lors du calcul avec l'algorithme RANSAC
    
    Le résultat est une détection de lignes plus épurée et plus précise que la référence
    
    """

    
    # Données de gauche (modifiées pour améliorer la performance de l'algorithme)
    Cleft = np.copy(C)
    Cleft[0:960, 575:1280] = 0

    # Prédiction à gauche (Vous ne devriez pas modifier cette section)
    leftdata = np.fliplr(np.argwhere(Cleft > 0))
    model_robust, inliers = ski.measure.ransac(leftdata, ski.measure.LineModelND, min_samples=50, residual_threshold=2, max_trials=1000)
    leftpos = model_robust.predict_x([750])
    yleft = model_robust.predict_y(xleft)
    
    # Données de droite (modifiées pour améliorer la performance de l'algorithme)
    Cright = np.copy(C)
    Cright[0:960, 0:575] = 0

    # Prédiction à droite (Vous ne devriez pas modifier cette section)
    rightdata = np.fliplr(np.argwhere(Cright > 0))
    model_robust, inliers = ski.measure.ransac(rightdata, ski.measure.LineModelND, min_samples=50, residual_threshold=2, max_trials=1000)
    rightpos = model_robust.predict_x([750])
    yright = model_robust.predict_y(xright)  

    # Affichage (Vous ne devriez pas modifier cette section)
    fig, axes = plt.subplots(1, 3, figsize=(15, 5), sharex=True, sharey=True)
    ax = axes.ravel()

    ax[0].imshow(img, cmap="gray")
    ax[0].set_title('Image')

    ax[1].imshow(mask, cmap="gray")
    ax[1].set_title('Lignes')

    ax[2].imshow(C * 0)
    ax[2].scatter(leftdata[:,0], leftdata[:,1], s=1, c='b')
    ax[2].scatter(rightdata[:,0], rightdata[:,1], s=1, c='g')
    
    ax[2].plot(xleft, yleft, c='r')
    ax[2].plot(xright, yright, c='r')

    ax[2].plot(np.mean([leftpos, rightpos]), 750, 'co')
    ax[2].plot(rightpos, 750, 'yo')
    ax[2].plot(leftpos, 750, 'yo')

    ax[2].set_xlim((0, img.shape[1]))
    ax[2].set_ylim((img.shape[0], 0))
    ax[2].set_title('Autopilot')

    for a in ax:
        a.set_axis_off()

    plt.tight_layout()
    plt.savefig('dataset/autopilot/output/Frame%i.png' % it)
    plt.close()
```

#### Code pour générer vidéo

```bash
#!/bin/bash

ffmpeg -framerate 25 -pattern_type glob -i '*.png' \
  -c:v libx264 -pix_fmt yuv420p out.mp4 -y

ffmpeg -framerate 25 -pattern_type glob -i 'Reference/*.png' \
  -c:v libx264 -pix_fmt yuv420p Reference/out.mp4 -y

ffmpeg -i out.mp4 -i Reference/out.mp4 -filter_complex vstack output.mp4 -y

```
