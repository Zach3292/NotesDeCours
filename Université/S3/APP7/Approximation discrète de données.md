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

Ça consiste à approximer un ensemble de points avec un certain nombre de coefficients polynomiaux.

### Approximation de fonction non linéaire
