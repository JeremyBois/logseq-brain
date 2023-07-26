tags:: Haskell
alias:: Haskell/Style
link:: [Kowainik](https://kowainik.github.io/posts/2019-02-06-style-guide) 
[[Jul 25th, 2023]]
***

- TODO Lire et ajouter notes sur la syntaxe
- ## Types
	- Utiliser `!` pour forcer une évaluation stricte des attributs
		- ```haskell
		  data Settings = Settings
		      { settingsHasTravis  :: !Bool
		      , settingsConfigPath :: !FilePath
		      , settingsRetryCount :: !Int
		      }
		  ```
		- Évite les *space leak*
		- Retourne une erreur si un champ est non initialisé
	-