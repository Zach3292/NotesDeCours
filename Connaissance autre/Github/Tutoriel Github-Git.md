## Définition
### Git
Git est un outil de contrôle de révision. Il permet de voir l'historique de modification d'un projet, de retourner à une version antérieur, d'avoir plusieurs versions du même projet en cours pour du développement et plein d'autres options. Il s'agit d'un outil très puissant lors du développement de toutes sortes de projet.

La structure d'un projet Git est basé sur un arbre avec des branches:
![branch](branch.png)

Il peut y avoir plusieurs branches en parallèle et il est aussi possible de combiner des branches ou d'en créer de nouvelles à partir d'une branche particulière. Dans un grand projet, la branche principale, souvent appelé *main* pourrait contenir la dernière version fonctionnelle du projet tandis que la branche *dev* pourrait contenir les nouveaux changements qui ne sont pas encore testés et prêts à être déployés. Ainsi, les développeurs peuvent travailler sur leurs produits sans avoir peur de rendre leur version actuelle non-fonctionnelle.

### Github
Github est une plateforme de développement qui permet d'héberger, de modifier, de gérer, de partager et de collaborer sur différents projets de programmation. Ce qui rend cette plateforme très utile est sa capacité de communiquer avec des projets Git sur des ordinateurs locaux. Ainsi, il est possible de synchroniser un projet Git sur son ordinateur personnel sur Github. En faisant cela, d'autres utilisateurs peuvent donc accéder à votre projet et collaborer, ou non. Github permet d'héberger votre projet dans le nuage gratuitement facilitant ainsi le déploiement et le développement sur plusieurs machines.

### Différence importante entre Git et Github
Même si les deux outils portent un nom similaire, ils n'ont pas la même utilité. Git permet de maintenir un historique de version et de gérer des branches en parallèle tandis que Github permet d'héberger les projets Git et de collaborer sur ceux-ci. Il est possible de collaborer sur des projets Git avec d'autres plateformes que Github tel que GitLab et Bitbucket mais Github demeure largement la plus populaire.

## Utilisation de Git
### Accéder à Git sur son ordinateur
#### Linux
Sur un ordinateur Linux, le logiciel Git est déjà installé et est accessible pour le biais du terminal. Pour vérifier l'installation de Git, exécuter la commande suivante:
```bash
git --version
```
#### Windows
**À venir**
### Créer un projet Git
Tout d'abord, il faut naviguer dans le dossier qui va contenir ou qui contient déjà votre projet. Ensuite, il faut exécuter la commande:
```bash
git init
```

Celle-ci va initialiser un répertoire Git dans votre dossier. Vous pouvez ensuite [ajouter des fichiers au projet](Tutoriel%20Github-Git.md#Ajouter%20des%20fichiers%20au%20projet) et [sauvegarder une version du projet](Tutoriel%20Github-Git.md#Sauvegarder%20une%20version%20du%20projet).
### Principales options de Git
#### Ajouter des fichiers au projet
Pour ajouter des fichiers présents dans le dossier au projet Git, il faut utiliser la commande suivante:
```bash
git add fichier.txt
```
Où fichier.txt est le nom du fichier. Pour ajouter tous les fichiers, exécuter la commande suivante:
```bash
git add .
```

Les changements dans les fichiers ajoutés seront ensuite suivis par Git.
#### Retirer des fichiers du projet
Pour arrêter de suivre les changements dans des fichiers particuliers, il faut utiliser la commande suivante avec les mêmes arguments que pour ajouter des fichiers:
```bash
git rm fichier.txt
```
#### Sauvegarder une version du projet
Pour sauvegarder une version du projet, il faut utiliser la commande suivante:
```bash
git commit -a -m "Message"
```
Dans cette commande, l'état de tous les fichiers qui avaient été ajoutés, modifiés ou retirer depuis la dernière sauvegarde va être enregistré avec le message passé en argument.
#### Créer une branche
Un des outils les plus puissant de Git est l'habileté de créer des branches. Pour créer une nouvelle branche à partir de la branche actuelle, il faut exécuter la commande suivante:
```bash
git branch maBranche
```
Où maBranche est le nom de la nouvelle branche qui sera créée. **Attention, la branche est seulement créer, vous êtes encore sur la branche originale.**
#### Voir la liste de branche
Pour voir la liste de branche existante:
```bash
git branch -l
```
#### Changer de branche
Pour changer de branche de travail:
```bash
git switch maBranche
```
Pour créer une branche en même temps que changer de branche:
```bash
git switch -c maBranche
```
#### Supprimer une branche
Pour supprimer une branche qui n'est plus utilisée ou nécessaire:
```bash
git branch -d maBranche
```
Où maBranche est le nom de la branche à supprimer
#### Renommer une branche
Pour renommer une branche avec un nouveau nom:
```bash
git branch -m maBranche maBrancheRenommer
```
#### Obtenir l'historique et les codes des versions
Pour obtenir l'historique et les codes des versions, il faut faire la commande suivante:
```bash
git log --stat
```
#### Observer la différence entre des versions
Pour observer une différence entre deux versions, il faut avoir les deux codes de version que l'on veut comparer et faire la commande suivante:
```bash
git diff codeV1 codeV2
```
#### Pour retourner voir une vieille version
#### Pour revenir sur la version à jour
#### Restaurer une ancienne version d'un fichier
#### Restaurer un fichier d'une autre branche

## Synchronisation avec Github
### Ajout d'un clé SSH à son compte Github
### Importer un projet Git sur Github
#### Synchroniser vos changements vers Github

### Cloner un projet de Github sur votre ordinateur
### Synchroniser des changements de Github sur votre ordinateur
#### Télécharger les changements sans les appliquer
#### Télécharger et appliquer les changements
#### Gérer des erreurs de synchronisation (merge-conflict)
### Ajouter des collaborateurs sur un projet Github
### Faire une fourche d'un projet public
### Faire une pull request sur un projet

## Utilisation de Git et Github dans Visual Studio Code
