Dans un système distribué, la communication joue un role clé. C'est grâce à elle que les différentes parties du système peuvent fonctionner.

### Types de communication
Une *communication persistante* est une communication dans laquelle l'envoyeur n'a pas besoin d'être actif après avoir envoyer son message, la communication va se faire quand même lorsque le receveur sera prêt. Une *communication transiente* par contre est seulement active lorsque le receveur et l'envoyeur sont actifs en même temps. Une communication peut aussi être *synchrone ou asynchrone*. Dans la première l'envoie bloque l'exécution de l'envoyeur jusqu'à ce qu'il reçoive confirmation du receveur.

### Remote procedure call
Il s'agit d'une méthode de communication où un ordinateur A appelle un procéder qui va s'exécuter sur un ordinateur B. De l'information est transporté entre les deux en paramètres et dans le résultats de l'appelle. On surnomme cette méthode **RPC**. 

Quand un procédé en appelle un autre par RPC, celui-ci se bloque temporairement en attendant les résultats. Comme s'il exécutait lui-même le procédé appelé. Pareil pour le serveur où le procédé est exécuté. Aux yeux de chaque procédé, ils ne "savent" pas que le procédé est appelé par une autre machine. Il s'agit simplement d'un appel local comme les autres. On peut résumer la communication RPC comme suit:
1. Le procédé client appelle un *client-stub* (un procédé local) d'une manière normal
2. Le stub construit le message et appelle le système d'opération local
3. L'OS du client envoie le message à l'OS du serveur
4. L'OS du serveur transmet le message au *server-stub*
5. Le stub déconstruit le message, les paramètres et appelle le serveur de manière local
6. Le serveur exécute l'appel comme si c'était un appel local (puisque à ses yeux s'en est un) et retourne le résultat au stub serveur
7. Le stub serveur construit le message et appelle l'OS du serveur
8. L'OS du serveur envoie le résultat à l'OS du client
9. L'OS du client transmet le résultat au client stub
10. Le client stub déconstruit le résultat et le transmet au procédé client qui le reçoit comme un résultat local (puisqu'à ses yeux s'en est un).

Un des défis du RPC est l'utilisation de pointeur et de référence puisque le serveur n'a pas accès à la mémoire du client. Il faut alors trouver un moyen de transmettre l'information pour qu'elle puisse être lu par n'importe quel autre acrhitecture. On règle souvent ces problèmes en utilkisant des manières d'encoder spécifique à des langages de programmation plus qu'