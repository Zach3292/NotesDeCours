### Les registres
Les registres consistent de variables **GLOBALES** aux programmes. Nous retrouvons des registres de différents types.

Exemples:
- Registre R[ ] – variable contenant entier ou réel;
- Registre de Position PR[ ] – Variables contenant une position;
- Registre de caractère SR[ ] – Variable contenant du texte
- Registres de vision VR[ ] – Variable contenant des données de vision artificielle
- Axes Registres de Positions;
- Registre de palettisation PL[ ].
- …

Pour afficher les registres, il faut: 
1. Appuyer sur le bouton Data 
2. Appuyer sur TYPE (F1),
#### Type de registre
##### Registre R[]
- Un registre est un espace mémoire de 32 bits réservé pour représenter un nombre.
- Il peut être un entier (INT32) ou un nombre réel (REAL32/FLOAT32)
##### Les Position Registre PR[]

- Position
    - X [REAL], Y [REAL], Z [REAL]
    - W [REAL], P [REAL], R [REAL]
- Références  
    - User Frame associé
    - User Tool Associé
- Configuration
    - F ou N
    - U ou D
    - T ou B
    - Nombre de tour des joints J1, J4, J6.
##### Les Strings Registre SR []

- Espace mémoire qui contient une liste de caractères (string).
### Instructions de programme
#### Instruction d’attente temporelle (WAIT)
Délai en seconde
#### Instructions de branche
- Une instruction de branche provoque le passage d’une ligne d’un programme à un autre. Quatre types d’instructions de branches sont possibles :
    - Instruction de label
    - Instruction de saut inconditionnel
    - Instruction de saut conditionnel
    - Instruction de fin de programme
##### Instructions de branche - étiquette (LBL)
- L’instruction d’étiquette _(label)_ LBL[i] est utilisée pour spécifier l’endroit où doit se brancher le programme d’exécution.
- Un commentaire peut être ajouté pour expliquer l’étiquette.
##### Instructions de branche – sauts inconditionnels (JMP LBL / CALL)
- Une instruction de saut inconditionnel cause invariablement un saut d’une ligne à une autre dans le même programme.
- Il existe deux types d’instructions de saut conditionnel :
    - Instruction Jump Label qui provoque un saut vers une étiquette (LBL).
##### Instructions de branche – sauts conditionnels (IF / SELECT)
- Une instruction de saut conditionnel provoque un saut d’une ligne à une autre lorsque certaines conditions sont satisfaites.
- Il existe deux types d’instructions de saut conditionnel :
    - Instruction de comparaison conditionnée (IF) : provoque un saut vers une étiquette ou un sous-programme lorsque certaines conditions sont satisfaites. L’instruction IF permet la comparaison de registre et d’E/S.
    - Instruction de sélection conditionnée (SELECT): provoque un saut vers une étiquette ou un sous-programme selon la valeur d’un registre.
#### Instruction boucle (FOR/ENDFOR)
- L’instruction FOR/ENDFOR est une fonction qui répète un nombre défini de fois toutes les instructions comprises entre FOR et ENDFOR.
- L’instruction FOR prend trois paramètres: un compteur de boucle, une valeur initiale et une valeur cible. Lorsque la valeur cible est supérieure à la valeur initiale, on utilise une incrémentation positive (TO) et lorsqu’elle est inférieure, une incrémentation négative (DOWNTO).
- L’instruction ENDFOR ne nécessite pas de paramètre.