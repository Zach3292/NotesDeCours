Lorsqu'on approxime, il faut définir un concept d'**erreur d'approximation** à chaque point: $$\delta_p=g(x_p)-y_p$$
Avec la somme de toutes ces erreurs, on trouve **l'erreur quadratique**: $$E=\sum_{p=1}^n{\delta_p^2}$$
### Approximation polynomiale
Formule MATLAB: 

```octave
function coeff = approx(x, y, M)
% approx computes the coefficients of a polynomial of degree M for a set of data points using the least squares method.

% Inputs:
% x - vector of x data points
% y - vector of function values at the data points
% M - degree of the polynomial

% Outputs:
% coeff - vector of coefficients of the polynomial

n = length(x);
if n < M + 1
	error('Number of data points must be at least M + 1');
end

B = zeros(1, M + 1);
for i = 1:M + 1
	B(i) = sum(y .* (x .^ (M + 1 - i)));
end

V = zeros(M + 1, M + 1);
for i = 1:M + 1
	for j = 1:M + 1
		V(i, j) = sum(x .^ ((M + 1 - i) + (M + 1 - j)));
	end
end

coeff = V \ B'; % Solve the linear system V * coeff = B
end
```

Ça consiste à approximer un ensemble de points avec un certain nombre de coefficients polynomiaux. Pour un système $AX+B=Y$, on a que $A$ est la matrice de coefficient, $$b_{ij}=\sum^N_{k=1}{y_kx_k^{M+1-k}}$$
$$x_{ij}=\sum^N_{k=1}{x^{2M+2-i-j}}$$

### Approximation de fonction non linéaire
On doit linéariser nos données avant de pouvoir utiliser la même méthode qu'avant. Par exemple, on peut linéariser une fonction exponentielle en appliquant un logarithme dessus.

Voici une liste des approximations à deux paramètres possibles:
- $\alpha e^{\beta x}$
- $\alpha x^\beta$
- $\alpha +\beta\ln{x}$
- $\alpha +\frac{\beta}{x}$
- $\frac{\alpha}{\beta+x}$
- $\frac{\alpha x}{\beta +x}$

En MATLAB la fonction suivante permet de trouver les coefficients de n'importe quelle distribution:
``` octave
x = [1,2,3,4,5];
y = [11.4,6.1,3.6,3.3,2.1];

coeff = polyfit(x, y, 2); % Fit a polynomial of degree 2
x_fit = linspace(min(x), max(x), 100);
y_fit = polyval(coeff, x_fit);
```
