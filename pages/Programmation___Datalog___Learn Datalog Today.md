type:: Book
author:: #[[Jonas Enlund]]
tags:: #Query #Datalog #BDD
alias:: Datalog/Learn Datalog Today 
link:: https://www.learndatalogtoday.org/
[[Mar 4th, 2023]]

- # Extensile data notation
	- type:: Article
	  link:: https://www.learndatalogtoday.org/chapter/0
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
	- type:: Article
	  link:: https://www.learndatalogtoday.org/chapter/1
	- Une [[base de données]] organisée autour d'une structure à plat formée de [[Datom]] qui est un Tuple de 4 éléments :
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
	- type:: Article
	  link:: https://www.learndatalogtoday.org/chapter/2
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
	- type:: Article
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
			- `:in $ ?director ?actor`
			- Permet de placer une valeur explicitement
		- Tuples
		  id:: 6406528f-d27a-4247-9202-3ca160ffd79a
			- `:in $ [?director ?actor]`
			- Permet de passer des tableaux et de les destructurer
		- Collections
			- `:in $ [?attr ...]`
			- Permet de passer plusieurs entrées (*List*)
				- Simule l'opérateur `or`
				- ```edn
				  [:find ?name
				   :in $ ?title [?attr ...]
				   :where
				   [?m :movie/title ?title]
				   [?m ?attr ?p]
				   [?p :person/name ?name]
				  ```
		- Relations
			- `:in $ ?director [[?title ?box-office]]`
			- Permet de passer un jeu de ((6406528f-d27a-4247-9202-3ca160ffd79a)) afin de réaliser des jointures avec la base de données
			- ```edn
			  [
			   ...
			   ["Die Hard" 140700000]
			   ["Alien" 104931801]
			   ["Lethal Weapon" 120207127]
			   ["Commando" 57491000]
			   ...
			  ]
			  
			  [:find ?title ?box-office
			   :in $ ?director [[?title ?box-office]]
			   :where
			   [?p :person/name ?director]
			   [?m :movie/director ?p]
			   [?m :movie/title ?title]]
			  ```
				- `?box-office` n'est pas utilisé dans la clause `:where`
					- Le trie est réalisé sur les `?title` uniquement
					- La **relation** permet de retrouver le nombre d'entrées
- # More queries
	- type:: Article
	  link:: https://www.learndatalogtoday.org/chapter/4
	- Attributs
		- Nom -> `:db/ident`
			- Chaque attribut est aussi une entité dans la base de donnée
		- Type --> `:db/valueType`
			- Type associé à l'attribut
				- `boolean`
				- `string`
				- ...
		- Cardinalité --> `:db/cardinality`
			- Quantité de valeur assignable
				- `one`
				- `many`
		- Liste --> `:db.install/attribute`
			- Liste complète des attributs dans la base de données
		- ```edn
		  [:find ?attr ?type ?card
		   :where
		   [_  :db.install/attribute ?a]
		   [?a :db/ident ?attr]
		   [?a :db/valueType ?t]
		   [?t :db/ident ?type]
		   [?a :db/cardinality ?c]
		   [?c :db/ident ?card]
		   ]
		  ```
	- Transactions
		- Temps associé à l'ajout dans la BDD --> `:db/txInstant`
			- ```edn
			  [:find ?timestamp
			   :where
			   [?p :person/name "James Cameron" ?tx]
			   [?tx :db/txInstant ?timestamp]]
			  ```
- # Predicates
	- type:: Article
	  link:: https://www.learndatalogtoday.org/chapter/5
	- Permet de filtrer les résultats
	- Trois écritures supportées
		-
		- Méthodes en [[Programmation/java]] --> `[(.startsWith ?name "M")]`
		  id:: 6407aca0-4234-426e-b109-cd31ed8c6199
		- Fonctions en [[Programmation/Closure]]  -->
			- Le namespace doit être compris
			-