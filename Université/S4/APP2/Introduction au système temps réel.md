### Définition
Un système temps réel est défini en deux critères:
1. Le temps que prend la réponse à être délivrée est aussi important que la qualité de la réponse
2. Les conséquences d'une réponse en retard sont aussi grave que les conséquences d'une mauvaise réponse.

Ce qui décrit comment un système réagit à l'état courant et au changement d'état sont appelés les *requis fonctionnels* (functional requirement). Tous les autres requis sont dit des *requis non-fonctionnels* (non-functional requirement).

Voici une liste de requis non-fonctionnels:
- Sécurité
- Performance
- Tolérance au faute
- Robustesse
- Évolutivité
- Sûreté

### Composantes d'un système temps réel
Il existe deux types de requis différents:
1. **Requis absolus** (absolute requirement): quand la réponse doit arriver à un moment définit
2. **Requis relatif** (relative requirement): quand la réponse doit arriver dans un interval de temps après un événement

Les conséquences de ne pas respecté les limites peuvent permettre de classifié encore plus les systèmes temps réel:
1. *Hard real-time*: Quand le fait de ne pas respecter le temps limite pour une réponse occasionne un échec du système et toute réponse par la suite n'a plus de valeur
2. *Firm real-time*: Quand le fait de ne pas respecter le temps limite pou une réponse n'occasionne pas d'échec mais toute réponse suivante n'a plus de valeur. Ça va causé une dégradation de la qualité du service.
3. *Soft real-time*: Quand la valeur d'une réponse diminue passé le temps limite mais qu'elle n'est pas inutile.