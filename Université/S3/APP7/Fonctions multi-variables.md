
### Définition
Plusieurs fonctions décrivant des phénomènes réels ne dépendant pas seulement d'une variable mais bien de plusieurs facteurs. On appelle ces fonctions des fonctions multi-variables. Par exemple: $$w=f(x_1,x_2,x_3)$$
Dans ce cas-ci, $w$ est une **variable dépendante** et $x_1,x_2,x_3$ sont des **variables indépendantes**. $f$ est une fonction multi-variables.

### Méthode de calcul
Prenons la fonction $z=xe^{-x^2-y^2}$:
#### Méthode par boucle
```octave
X = linspace(-2, 2, 20);
Y = linspace(-2, 2, 30);

for ix=1:length(X)
	for iy=1:length(Y)
		Z(ix, iy) = X(ix)*exp(-X(ix)^2-Y(iy)^2)
	end
end
```

#### Méthode matricielle
```octave
X = linspace(-2,2,20); 
Y = linspace(-2,2,30); 

% Creation de matrices pour X et Y 
[Xmat,Ymat] = meshgrid(X,Y); 

% Calcul matriciel 
Z = Xmat .* exp(-Xmat.^2-Ymat.^2)
```

### Représentation
#### Méthode du surf
```octave
surf(X,Y,Z) 
xlabel('x') 
ylabel('y') 
zlabel('f(x,y)') 
box on; 
grid on;
```
#### Méthode des lignes de contour
```octave
contour3(X,Y,Z,30) 
xlabel('x') 
ylabel('y') 
zlabel('f(x,y)') 
box on; 
grid on;
```
#### Méthode par image
```octave
imagesc(X,Y,Z) 
xlabel('x') 
ylabel('y') 
box on; 
grid on; 
colorbar('vert')
```
#### Méthode par lignes de niveau
```octave
contour(X,Y,Z) 
xlabel('x') 
ylabel('y') 
box on; 
grid on; 
colorbar('vert')
```

### Dérivées partielles
Comme les fonctions varient maintenant selon plusieurs variables, il est important de définir un opération de dérivée. On va évaluer le changement par rapport à une seule variable en considérant les autres comme des constantes. On appelle ça faire de la dérivation partielle:
$$\frac{\partial f}{\partial x_1}(x_1^0,x_2^0,...,x_n^0)$$
On dit ici qu'on évalue la dérivée partielle de $f$ en fonction de $x_i$ au point $(x_1^0,x_2^0,...,x_n^0)$.
#### Recherche des extremums d'une fonction
Pour calculer les extremums de fonction multi-variables, il faut trouver les **points critiques**. Il s'agit des points où:
$$\frac{\partial}{\partial x_i}(x_1,x_2,...,x_n)=0 \ \forall i= 1...n$$ 
Pour savoir quel type de point critique il s'agit, on dispose du théorème suivant pour les fonctions à deux variables:

Si: $$\frac{\partial^2 f}{\partial x^2}(a,b)<0 \textrm{ et } \frac{\partial^2 f}{\partial x^2}(a,b)\frac{\partial^2 f}{\partial y^2}-\left[\frac{\partial^2 f}{\partial x\partial y}(a,b)\right]^2>0$$
Alors maximum local. Si: $$\frac{\partial^2 f}{\partial x^2}(a,b)>0 \textrm{ et } \frac{\partial^2 f}{\partial x^2}(a,b)\frac{\partial^2 f}{\partial y^2}-\left[\frac{\partial^2 f}{\partial x\partial y}(a,b)\right]^2>0$$
Alors minimum local. SI: $$\frac{\partial^2 f}{\partial x^2}(a,b)\frac{\partial^2 f}{\partial y^2}-\left[\frac{\partial^2 f}{\partial x\partial y}(a,b)\right]^2<0$$
Alors point de selle. Si: $$\frac{\partial^2 f}{\partial x^2}(a,b)\frac{\partial^2 f}{\partial y^2}-\left[\frac{\partial^2 f}{\partial x\partial y}(a,b)\right]^2=0$$
Alors on ne peut pas conclure.
#### Dérivée partielle d'ordre supérieur
Lorsqu'elle existe, on définit les dérivées partielles d'ordre supérieur comme suit:$$\frac{\partial}{\partial x_i}\left(\frac{\partial f}{\partial x_j}\right)=\frac{\partial^2 f}{\partial x_i\partial x_j}(x_1,x_2,...,x_n)$$
Aussi:
$$\frac{\partial^2 f}{\partial x\partial y}(x^0,y^0)=\frac{\partial^2 f}{\partial y\partial x}(x^0, y^0)$$

### Différentiation totale
#### Linéarisation d'une fonction multi-variables
Si un point est suffisamment près d'un autre point, alors:$$f(x_1,...,x_n)\approx L(x_i,...,x_n)= f(x_1^0,...,x_n^0)+\sum^{n}_{i=1}{\frac{\partial f}{\partial x_i}(x_i^0,...,x_n^0)(x_i-x_i^0)}$$
Où $L(x_i,...,x_n)$ est la linéarisation de la fonction $f$ autour du point $(x_i^0,...,x_n^0)$.
#### Différentielle totale
On définit la différentielle totale $df$ comme: $$df=\sum^{n}_{i=1}{\frac{\partial f}{\partial x_i}(x_i^0,...,x_n^0)dx_i}$$ Il s'agit de la variation de la fonction $f$ lorsque toutes les variables $x_i$ varient de $dx_i$ autour du point $(x_i^0,...,x_n^0)$.


