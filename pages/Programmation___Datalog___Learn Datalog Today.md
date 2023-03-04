tags:: #Formation #Query 
alias:: Datalog/Learn Datalog Today 
link:: https://www.learndatalogtoday.org/
[[Mar 4th, 2023]]

- # Extensile data notation
	- link:: https://www.learndatalogtoday.org/chapter/0
	- `.edn` = Extensible Data Notation
	- Format utilisé pour écrire les requêtes
		- Similaire à du [[JSON]] sur le format
		- Extensible avec des types propres à l'utilisateur
		- Plus de types de base
		- Sous-ensemble des structures de données de [[Closure]]
	- Exemple de requête
		- ``` edn
		  [:find ?title
		   :where 
		   [_ :movie/title ?title]]
		  ```
- # Requêtes basiques
	- link:: https://www.learndatalogtoday.org/chapter/1
	- Une  organisée autour de [[Datom]]
	- Une requête est un vecteur
		- ```edn
		  [:find ?e ?title
		   :where
		   [?e :movie/title ?title]]
		  ```
		-
		-
		-