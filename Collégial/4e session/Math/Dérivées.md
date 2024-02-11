#### Forward difference
$$f'(a) \approx \frac{f(a+h)-f(a)}{h}$$
#### Backward difference
$$f'(a) \approx \frac{f(a)-f(a-h)}{h}$$
#### Central difference
$$f'(a) \approx \frac{f(a+h)-f(a-h)}{2h}$$
#### Polynôme de Taylor
$$ T_n (x) = \sum_{k=0}^{n} \frac{f^{(k)} (a)}{k!} (x-a)^k$$
#### Dérivée deux dimensions
1. Il faut calculer la dérivée partielle de chaque dimension soit:
	$$ \frac{\delta f(x, y)}{\delta x} et \frac{\delta f(x, y)}{\delta y}$$
2. Ensuite, il faut créer un vecteur ayant comme composantes les deux dérivées partielles. Celui-ci s'appelle le gradient
	$$\vec{G} = \left[ \frac{\delta f(x, y)}{\delta x} \;\;\; \frac{\delta f(x, y)}{\delta y}\right]$$
3. La norme du gradient correspond à la dérivée deux dimensions de la fonctions
		$$ ||G|| = \sqrt{{\left(\frac{\delta f(x, y)}{\delta x}\right)}^2+{\left(\frac{\delta f(x, y)}{\delta y}\right)}^2}$$
