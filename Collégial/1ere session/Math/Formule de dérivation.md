### Formule de base
$$\frac{dk}{dx}=0$$
$$\frac{dx}{dx}=1$$
$$\frac{dku}{dx}=k\frac{du}{dx}$$
$$\frac{d(u\pm v)}{dx}=\frac{du}{dx}\pm\frac{dv}{dx}$$
$$\frac{d(u\cdot v)}{dx}=u\frac{dv}{dx}+v\frac{du}{dx}$$
$$\frac{d(u/v)}{dx}=\frac{v\frac{du}{dx}-u\frac{dv}{dx}}{v^2}$$
$$\frac{dx^n}{dx}=nx^{n-1}$$
$$\frac{du^n}{dx}=nu^{n-1}\frac{du}{dx}$$
### Dérivée implicite
On interprète y comme une fonction, exemple:
$$\begin{align}
x^2 + y^2 & = 9 \\
\frac{dx^2}{dx}+\frac{dy^2}{dx}&=0 \\
2x+2y\frac{dy}{dx}&=0 \\
\frac{dy}{dx}&=\frac{-x}{y} \\
\end{align}$$
### Dérivée de fonction transcendante
#### Exponentielles
$$\frac{db^u}{dx}=b^u\cdot\ln{b}\cdot\frac{du}{dx}$$
#### Logarithmes
$$\frac{d\log_b{u}}{dx}=\frac{1}{u\cdot\ln{b}}\cdot\frac{du}{dx}$$
Une technique de dérivation s'appelle la dérivation logarithmique, exemple:
$$y=x^x$$
$$\ln{y}=\ln{x}^x$$
$$\ln{y}=x\ln{x}$$
#### Trigonométriques
$$\frac{d\sin{u}}{dx}=\cos{u}\cdot\frac{du}{dx}$$$$\frac{d\cos{u}}{dx}=-\sin{u}\cdot\frac{du}{dx}$$
$$\frac{d\tan{u}}{dx}=\sec^2{u}\cdot\frac{du}{dx}$$
$$\frac{d\sec{u}}{dx}=\sec{u}\tan{u}\cdot\frac{du}{dx}$$
$$\frac{d\csc{u}}{dx}=-\csc{u}\cot{u}\cdot\frac{du}{dx}$$
#### Trigonométriques inverses
$$\frac{d\arcsin{u}}{dx}=\frac{1}{\sqrt{1-u^2}}\cdot\frac{du}{dx}$$
$$\frac{d\arccos{u}}{dx}=\frac{-1}{\sqrt{1-u^2}}\cdot\frac{du}{dx}$$
$$\frac{d\arctan{u}}{dx}=\frac{1}{1+u^2}\cdot\frac{du}{dx}$$