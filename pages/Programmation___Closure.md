tags:: Dynamique
alias:: Closure
link:: https://clojure.org/
[[Apr 21st, 2023]]
***

- Un dialecte de [[Programmation/Lisp]] [[Programmation/Dynamique]]
	- Pensé pour la programmation concurrente
	- Fonctionnement immutable par défaut
	- Plus de sucre syntaxique que dans [[Programmation/Lisp]] mais moins générique
	- Approche fonctionnelle
	- Runtime pour la [JVM](https://fr.wikipedia.org/wiki/Machine_virtuelle_Java) le rendant compatible avec une large palette de codes existants
- De nombreux outils pour aider le dévelopeur
	- *Live coding* avec [Clerk](https://clerk.vision/)
		- Notebook sans les faiblesses inhérentes aux Jupyter notebook
			- Pas de nouveaux éditeur mais une ompatibilité avec le format de fichier classique
				- Possible d'ajouter des informations en markdown
			- Pas un format de fichier particulier
		- Outils graphiques pour visualiser les données et les algorithmes