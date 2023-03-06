tags:: #Formation #Query #Datomic 
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
		- Commencer une reqûete -->`:find` suivie de variables *patterns* (`?e`, `?title`)
		- Restreindre les résultats et associer la recherche à un *pattern* --> `:where`
		- ```edn
		  [:find ?e ?title
		   :where
		   [?e :movie/title ?title]]
		  ```
		- Ignorer une partie non utile avec un joker (*wildcard*)--> `_`
			- ```edn
			  [:find ?e
			   :where
			   [?e :person/name "Ridley Scott" _]]
			  ```
			-
- # Data pattern
	- link:: https://www.learndatalogtoday.org/chapter/2
	- Une `where` clause peut contenir plusieurs *data patterns* afin de construire des **jointures**
		- Une même *variable pattern* peut être réutilisée
		- ```edn
		  [:find ?title
		   :where
		   [?e :movie/year 1987]
		   [?e :movie/title ?title]]
		  ```
	- Possible de relier plusieurs *variables pattern* pour cumuler des filtres :
		- Exemple : Récupère le nom des personnes (stockées dans `?p`) pour les films dans lesquels elles participent (stockée dans `?m`) dont le titre est `"Lethal Weapon"` (stockée dans `?m`)
			- ```edn
			  [:find ?name
			   :where
			   [?m :movie/title "Lethal Weapon"]
			   [?m :movie/cast ?p]
			   [?p :person/name ?name]]
			  ```
	- L'ordre des contraintes n'a pas d'importance même si les données sont connectées
		- Les clauses suivantes sont donc équivalentes
			- ```edn
			  [:find ?name
			   :where
			   [?d :person/name ?name]
			   [?m :movie/director ?d]
			   [?m :movie/cast ?p]
			   [?p :person/name "Arnold Schwarzenegger"]]
			  ```
			- ```edn
			  [:find ?name
			   :where
			   [?p :person/name "Arnold Schwarzenegger"]
			   [?m :movie/cast ?p]
			   [?m :movie/director ?d]
			   [?d :person/name ?name]]
			  ```
- # Parameterized queries
	- type:: Book
	  link::  https://www.learndatalogtoday.org/chapter/3
	- Possible de passer des arguments --> `:in`
		- ```edn
		  [:find ?title
		   :in $ ?name
		   :where
		   [?p :person/name ?name]
		   [?m :movie/cast ?p]
		   [?m :movie/title ?title]]
		  ```
		- `$` représente la base de données
			- Implicite si il n'y a pas de clause `:in`
	- Types existants :
		- Scalaires (*Scalars*)
		- Tuples
			- `[?name ?age]`
		- Collections
		- Relations
		-
		-