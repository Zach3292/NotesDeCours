### Hiérarchie de réduction des risques, élimination du risque et conception sûre de la machine
![|300](Images/Pasted%20image%2020250412102004.png)
Une fois les mesures correctives mises en place, il faut refaire l’analyse des risques pour s’assurer que de nouveaux risques n’ont pas été introduits sans le vouloir.
![|300](Images/Pasted%20image%2020250412102038.png)
#### Élimination des risques
**Éliminer le risque**, cela signifie opter pour un autre procédé ou une autre machine qui ne représente pas un risque pour la sécurité ou qui représente un risque différent et plus facile à atténuer ensuite par d’autres méthodes

#### Conception de machine sûre
Pour concevoir une **machine sûre**, il faut par exemple: 
- écarter les pièces mobiles 
	- distances de sécurité minimales à respecter afin de s’assurer qu’une personne ou qu’un membre ne soit coincé entre la pièce mobile et une autre pièce.
- éliminer les arêtes vives et les points de cisaillement 
	- ![|200](Images/Pasted%20image%2020250412102336.png)
- limiter les efforts d’entraînement 
- limiter les niveaux d’énergie 
- éliminer l’énergie potentielle accumulée en cas de panne 
- appliquer adéquatement les principes d’ergonomie

### Protecteurs et dispositifs de protection
On réduit le risque en empêchant une personne de se retrouver dans une zone dangereuse à l’aide de protecteurs et de dispositifs de protection.

Un **protecteur** est une barrière physique qui bloque l’accès à la zone dangereuse.
- Protecteur fixe
- Protecteur à verrouillage
	- L’élément de contact qui sert de moyen de détection de l’ouverture du protecteur possède un lien mécanique direct avec le protecteur.
- Protecteur à enclenchement

#### Dispositif de protection

Un **dispositif de protection** sert à arrêter le mouvement d’une machine, sur demande ou lorsqu’une personne pénètre dans la zone dangereuse.

Un arrêt **forcé** coupe la commande au système automatisé, mais le circuit *demeure actif* et prêt à redémarrer.

Un arrêt d’**urgence** déclenche le système de sécurité et empêche l’activation du système automatisé

Un **automate de sécurité** diffère d’un automate conventionnel, entre autres par sa capacité à gérer la sécurité d’un système automatisé. Pour cela il utilise : 
1. une architecture redondante 
2. des routines de diagnostics pour vérifier l’état des E/S de l’automate 

Les boutons d’arrêt d’urgence, les capteurs de sécurité (scanneurs de zone, rideaux virtuels, etc.) et les autres dispositifs de sécurité sont donc reliés à un **automate de sécurité.**

Dans certains cas, on utilisera un **relais de sécurité** sur un automate conventionnel pour lui ajouter les fonctionnalités de sécurité

Il faut faire attention avec l'utilisation de **contact normalement ouvert ou fermé**. Il faut choisir le bon selon la situation
##### Différent dispositif de protection
**Commande bimanuelle**: Une commande bimanuelle nécessite l’appui simultané sur deux boutons pour activer le mouvement d’une machine. Cela assure que les deux mains d’une personne ne sont pas situées dans la zone dangereuse.

**Rideau virtuel**: Franchir un rideau virtuel vertical fera arrêter la machine ou le robot. Cela donne accès à la zone de travail plus facilement qu’avec un protecteur, mais ne constitue pas une barrière contre les éclats physiques projetés.

**Scanneur de zone**: Un scanneur de zone détecte avec précision l’approche d’une personne, mais seulement à une certaine hauteur au-dessus du sol. On peut alors décider d’arrêter la machine ou d’en réduire progressivement la vitesse

#### Niveau de performance
Devant une situation à risque, comment choisir un dispositif de protection plutôt qu’un autre? Il faut s’assurer que son **niveau de performance** (en anglais performance level ou **PL**) est adéquat pour le niveau de risque identifié.

On définit le **PL** d’un équipement et le PL minimum requis (**PLr**) pour une situation à risque.
