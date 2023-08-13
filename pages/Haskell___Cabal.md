tags:: Haskell
link:: https://www.haskell.org/cabal/
[[Jul 25th, 2023]]
***

- DOING Récupérer les notes de Obsidian
- # Définition
	- Cabal peut correspondre à plusieurs choses
		- *cabal-install*
			- Outil de build pour Haskell
				- Test, Exe, Lib
			- Gestion des dépendances
				- Sandbox
				- Téléchargement des packages
		- `.cabal`
			- Format des fichiers de configuration utilisés par *cabal-install*
		- *Cabal*
			- Bibliothèque implémentant un parseur pour les fichiers `.cabal` afin de les utiliser avec *cabal-install*
- ## Cabal-install
	- Installation avec #Haskell/ghcup
	- ```bash
	  ghcup install cabal
	  ```
		- Construit un raccourci à`~/.ghcup/bin/cabal`
	-