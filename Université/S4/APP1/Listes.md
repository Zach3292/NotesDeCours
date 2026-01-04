Une liste est une structure de données de base en Python. Elle possède plusieurs opérations qui permettent d’interagir avec elle.

### Liste non-ordonnée
Il s'agit de la liste de base qui possède des items et leur position relative entre eux. Il existe plusieurs méthodes pour interagir avec ces listes:
```python
List() # Crée une liste vide
add(item) # Ajoute un item àu début de la liste
remove(item) # Retire un item de la liste
search(item) # Retourne si un item est présent dans la liste
is_empty() # Retourne si la liste est vide
size() # Retourne la taille de la liste
append(item) # Ajoute un item à la fin de la liste
index(item) # Retourne la position d'un item dans la liste
insert(position,item) # Insère un item à la position voulue dans la liste
pop() # Retire et retourne le dernier élément de la lsite
pop(position) # Retire et retouren l'item à la position voulue de la liste
```
#### Implémentation
Pour créer une liste non-ordonnée, on peut utiliser le concept d'une liste chaînée. Une liste chaînée est un ensemble d'item qui contiennent tous: une donnée, un lien vers la prochain item. On appelle ces items des *nœuds*.
![](Images/linkedlist.png)
Voici les implémentations de certaines fonctions de base d'une liste chaînée:
```python
def add(self, item):
	temp = Node(item)
	temp.set_next(self.head)
	self.head = temp
```
```python
def size(self):
	current = self.head
	count = 0
	while current != None:
		count = count + 1
		current = current.get_next()
	return count
```
```python
def search(self,item):
	current = self.head
	found = False
	while current != None and not found:
		if current.get_data() == item:
			found = True
		else:
			current = current.get_next()
	return found
```
```python
def remove(self, item):
	current = self.head
	previous = None
	found = False
	while not found:
		if current.get_data() == item:
			found = True
		else:
			previous = current
			current = current.get_next()
	if previous == None:
		self.head = current.get_next()
	else:
		previous.set_next(current.get_next())
```
### Liste ordonnée
Une liste ordonnée est très similaire à une liste non-ordonnée avec pour seule différence que les éléments dans la liste sont en ordre croissant. Cela modifie quelque fonction comme la fonction add() qui doit maintenant placer les items au bon endroit et non pas au début. Cela fait que cette méthode passe de $O(1)$ pour une liste non-ordonnée à $O(n)$ pour une liste ordonnée.