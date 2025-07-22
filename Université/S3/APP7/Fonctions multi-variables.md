
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
