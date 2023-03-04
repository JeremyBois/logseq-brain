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
	- Une [[base de données]] organisée autour d'une structure à plat formée de [[Datom]]
		- Entity ID
		- Attribut
		- Valeur
		- Transaction ID
	- Une requête est représenté comme un vecteur
		- Commence par le mot clé `:find` suivie de *patterns* (`?e`, `?title`)
		- Utilisation possible de la clause `where` pour restreindre les résultats et associée la recherche à un *pattern*
		- ```edn
		  [:find ?e ?title
		   :where
		   [?e :movie/title ?title]]
		  ```
		- Possible d'utiliser `_` comme un **joker** pour ignorer une partie
			-
			-