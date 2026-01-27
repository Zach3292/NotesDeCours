### Définition
Un système temps réel est défini en deux critères:
1. Le temps que prend la réponse à être délivrée est aussi important que la qualité de la réponse
2. Les conséquences d'une réponse en retard sont aussi grave que les conséquences d'une mauvaise réponse.

Ce qui décrit comment un système réagit à l'état courant et au changement d'état sont appelés les *requis fonctionnels* (functional requirement). Tous les autres requis sont dit des *requis non-fonctionnels* (non-functional requirement).

Voici une liste de requis non-fonctionnels:
- Sécurité: réponses du système qui le protège des dommages
- Performance: timing ou vitesse nécessaire pour empêcher le système de subir des dommages
- Tolérance au faute: L'habileté de protéger le système des fautes de design
- Robustesse: L'habileté de protéger le système des fautes externes
- Évolutivité: L'habileté de performer correctement dan un environnement avec plus de charge
- Sûreté: L'habileté du système à résister à des opérations qui sont voulues pour causé des dommages

### Composantes d'un système temps réel
Il existe deux types de requis différents:
1. **Requis absolus** (absolute requirement): quand la réponse doit arriver à un moment définit
2. **Requis relatif** (relative requirement): quand la réponse doit arriver dans un interval de temps après un événement

### Classement des systèmes
Les conséquences de ne pas respecté les limites peuvent permettre de classifié encore plus les systèmes temps réel:
1. *Hard real-time*: Quand le fait de ne pas respecter le temps limite pour une réponse occasionne **un échec du système** et toute réponse par la suite n'a plus de valeur.
2. *Firm real-time*: Quand le fait de ne pas respecter le temps limite pour une réponse n'occasionne pas d'échec mais **toute réponse suivante n'a plus de valeur**. Ça va causé une dégradation de la qualité du service. *Exemple: prévision météo qui arrive le lendemain de la date.*
3. *Soft real-time*: Quand **la valeur d'une réponse diminue** passé le temps limite mais qu'elle **n'est pas inutile**. Dépassé le temps limite n'apporte aucune autre implication.