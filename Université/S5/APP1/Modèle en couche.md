Pour réduire la complexité, la plupart des réseaux sont organisés en couches ou en niveaux. Les couches respectent une hiérarchie et chaque couche parle directement à la couche qui la précède et à la suivante. On trouve une interface entre une paire de couches adjacentes. Pour un bone modèle en couche, on peut changer la couche inférieur sans affecter les couches supérieurs.

### Service avec connexion
Un service avec connexion suit le modèle téléphonique. On contact quelqu'un, il décroche et répond et ensuite on raccroche. On doit donc commencer par établir une connexion. Ensuite on discute et finalement on ferme la connexion. 
### Service sans connexion
Il s'agit d'un service qui envopie de l'ionformation sans avoir de communication avec un autre. Il envoie et si quelqu'un écoute à ce moment, il va recevoir. Chaque type de service à ses avantages et ses inconvénients.
### Différence entre service et protocole
Un service est un ensemble de primitives (opérations) qu'une couche fourni à la couche supérieur. Il définit des opérations que la couche est prête à exécuter. Il se rapporte par une interface, la couche inférieure étant le fournisseur de service et la couche supérieure est l'utilisateur du service.

Un protocole est un ensemble de règles qui déterminent le format et la signification des paquets ou des messages envoyés. 

En résumé, les services se rapportent aux interfaces entre des couches et les protocoles se rapportent aux paquets qui sont échangés par deux entités paires sur deux machines différentes.

### Modèle de référence OSI
Il est composé de trois concepts:
1. Les services
2. Les interfaces
3. Les protocoles
Il comporte sept couches:
- Application
- Présentation
- Session
- Transport
- Réseau
- Liaison de données
- Physique
![](Images/Pasted%20image%2020260905182636.png)
Pour choisir ces couches les principes suivants ont été choisis:
1. Une couche doit être créée lorsqu'un nouveau niveau d'abstraction est nécessaire
2. Chaque couche doit assurer une fonction bien définie
3. La fonction de chaque couche doit être choisie en visant la définition de protocoles normalisés au niveau international.
4. Les limites d'une couche doivent être fixées de manière à réduire la quantité d'informations devant passer au travers des interfaces.
5. Le nombre de couche doit être, d'une part, assez grand pour que des fonctions très distinctes ne soient pas regroupées dans une même couche et, d'autre part, suffisamment faible pour que l'architecture ne devienne pas trop complexe
### Modèle de référence TCP/IP
Il s'agit d'un modèle en couche utilisé grandement par l'internet.
![](Images/Pasted%20image%2020260905182710.png)
![](Images/Pasted%20image%2020260905182723.png)
#### La couche liaison
La plus basse du modèle, elle décrit ce que les liens comme les lignes séries et les connexions Ethernet classiques doivent faire
#### La couche internet 
Elle est l'axe centrale qui correspond majoritairement à la couche réseau du modèle OSI. Le rôle de la couche est d'Acheminer les paquets IP à leur destination.
#### La couche transport
Directement supérieur à la couche internet, son rôle est de permettre à des entités paires de mener une conversation. Deux protocoles ont été définis **TCP et UDP**. TCP est un protocole fiable avec connexion qui garantie la livraison sans erreur des messages. UDP est un protocole non fiable sans connexion qui permet aux applications d'assurer elles-mêmes le séquençage et le contrôle de flux. Elle est plus rapide que TCP.
#### La couche application
Elle contient tous les protocoles hauts niveaux utilisés par les applications comme HHTP, DNS, FTP etc.