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
		- ```
		  [<e-id>  <attribute>      <value>          <tx-id>]
		  ...
		  [ 167    :person/name     "James Cameron"    102  ]
		  [ 234    :movie/title     "Die Hard"         102  ]
		  [ 234    :movie/year      1987               102  ]
		  [ 235    :movie/title     "Terminator"       102  ]
		  [ 235    :movie/director  167                102  ]
		  ...
		  ```
	- Une requête est représentée comme un vecteur :
		- Commence par le mot clé `:find` suivie de variables *patterns* (`?e`, `?title`)
		- Utilisation possible de la clause `where` pour restreindre les résultats et associer la recherche à un *pattern*
		- ```edn
		  [:find ?e ?title
		   :where
		   [?e :movie/title ?title]]
		  ```
		- Possible d'utiliser `_` comme un **joker** pour ignorer une partie non utile
			- ```edn
			  [:find ?e
			   :where
			   [?e :person/name "Ridley Scott" _]]
			  ```
			-
- # Data pattern
	- link:: https://www.learndatalogtoday.org/chapter/2
	- Une `where` clause peut contenir plusieurs *data patterns*
		- Une même *variable pattern* peut être utilisée sur chaque *pattern* afin de cumuler les contraintes
		- L'ordre n'a pas d'importance (les clauses suivantes sont donc équivalentes)
			- ```edn
			  [?e :movie/year 1987]
			   [?e :movie/title ?title]]
			  ```
			- ```edn
			  [?e :movie/title ?title]
			   [?e :movie/year 1987]]
			  ```
	-