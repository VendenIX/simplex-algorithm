simplex-algorithm
=================

Python source code for [Linear Programming and the Simplex Algorithm](http://jeremykun.com/2014/12/01/linear-programming-and-the-simplex-algorithm/)


Ce que le code prend en charge :

	1.	Problèmes de maximisation :
Le code est conçu pour résoudre les problèmes de maximisation, où l’objectif est de maximiser une fonction objectif sous des contraintes d’inégalité.
	2.	Contraintes d’inégalité (￼) :
Le code peut gérer les contraintes de type ￼ en ajoutant des variables d’écart pour transformer les inégalités en égalités.
	3.	Variables non négatives :
Les variables ￼, ￼ sont bien gérées.

Ce que le code ne prend pas en charge directement :

	1.	Problèmes de minimisation :
Si tu veux résoudre un problème de minimisation, tu devras ajuster manuellement le code pour inverser la fonction objectif. Une façon simple de le faire est de multiplier les coefficients de la fonction objectif par ￼, et ensuite de maximiser cette nouvelle fonction.
Exemple : Pour minimiser ￼, tu transformes cela en maximiser ￼.
Le code pourrait être modifié pour automatiquement gérer ce cas en ajoutant un paramètre pour spécifier si le problème est de maximisation ou de minimisation.
	2.	Contraintes d’inégalité (￼) :
Actuellement, le code gère seulement les inégalités du type ￼. Pour des inégalités du type ￼, tu devrais ajouter des variables d’excès au lieu de variables d’écart. Cela nécessite quelques modifications dans le code.
Par exemple, pour une contrainte ￼, tu introduis une variable ￼ telle que :
￼
Le code pourrait être modifié pour détecter automatiquement les inégalités du type ￼ et ajouter les variables d’excès nécessaires.
	3.	Contraintes d’égalité :
Si tu as des contraintes d’égalité ￼ dans ton problème, comme ￼, tu devras les gérer manuellement dans le code. Le code actuel ne supporte que les inégalités et les contraintes d’égalité nécessitent généralement des ajustements spécifiques dans l’algorithme du simplexe.
	4.	Variables libres (non bornées) :
Le code assume que toutes les variables sont ￼ (non négatives). Si tu as des variables libres (qui peuvent être négatives), il faudrait les transformer en deux variables non négatives (comme expliqué dans le concept des variables libres).
Par exemple, pour une variable ￼, tu pourrais la transformer en ￼ avec ￼ et ￼.
	5.	Problèmes plus complexes :
Le code ne prend pas en compte les problèmes qui impliquent des variantes du simplexe, comme le simplexe dual, qui est utile pour certains types de problèmes plus complexes ou mal conditionnés.

Ajustements potentiels pour généraliser le code :

	1.	Prise en charge des minimisations :
Tu peux modifier la ligne où la fonction objectif est définie pour inclure une option de minimisation en inversant automatiquement les coefficients si c’est un problème de minimisation.
	2.	Détection automatique des inégalités (￼) :
Tu peux étendre le code pour détecter les inégalités du type ￼ et ajouter des variables d’excès comme expliqué plus haut.
	3.	Gestion des contraintes d’égalité :
Tu pourrais modifier le code pour ajouter une gestion des contraintes d’égalité dans les systèmes de contraintes.
	4.	Variables non bornées :
Ajouter une transformation pour les variables libres non bornées afin de les traiter avec deux variables positives.

En résumé :

Le code actuel fonctionne bien pour les problèmes de maximisation avec des contraintes d’inégalité ￼, mais pour prendre en charge des problèmes plus généraux (minimisation, ￼, égalités, variables libres), il nécessiterait quelques ajustements.

Si tu veux explorer un plus large éventail de problèmes de programmation linéaire, je peux t’aider à modifier le code en fonction des besoins spécifiques que tu rencontres.