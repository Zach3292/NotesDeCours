### Espace de nom (namespace)
Un espace de nom est utile pour regrouper des définitions et éviter de polluer l'espace global accessible en tout temps. On accède à ses espaces avec le symbole ::

```cpp
std::cout << "Accès à l'espace de la librairie standard" << std::endl;
```

L’utilisation des espaces de nom permet d'éviter les duplications de nom de méthode lorsque plusieurs librairies ou programmes ont des fonctions portant le même nom.

#### Création d'espace de nom
On peut déclarer ce que l'on veut dans un espace de nom pour l'utiliser plus tard, voici un exemple 
```cpp
# include < cstdio > 
# include < thread >
namespace gro { 
	class Exemple // D ´e finition de classe .
	{ 
		private : 
			int membre_ ; 
		public : 
			Exemple ( int i) // Constructeur . 
			{ 
				membre_ = i; 
			} 
			void print () const 
			{ 
				printf (" Exemple % i\n" , membre_ );
			}
			void operator ()() const 
			{ 
				printf (" Objet - fonction %i\ n" , 
				membre_ ); 
				while ( true ) {}; // Boucle infinie . 
			} 
	};
} 

int main ( int argc , char ** argv ) 
{ 
	gro :: Exemple ex1 (1); 
	gro :: Exemple ex2 (2); 
	
	ex1 . print (); // Affiche " Exemple 1". 
	ex2 . print (); // Affiche " Exemple 2". 
	// ex1 . membre_ = 3; // Erreur : membre_ est priv ´e . 
	
	gro :: Exemple ex3 (3); 
	
	std :: thread fil ( ex3 ); // D ´e marre un nouveau fil , 
	// affiche " Objet - fonction 3". 
	
	while ( true ) {}; // Boucle infinie . 
	
	return 0;
}
```

### Importation de la librairie standard de C
On peut quand même utiliser la libraire de base du language C en C++ comme suit:
```cpp
#include <cstdio>
```
La convention veut qu'on ne met pas le .h lorsqu'il s'agit de librairies standards.

