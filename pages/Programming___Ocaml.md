tags:: Functional, OOP
alias:: Ocaml
link:: https://ocaml.org/ 
[[Jul 21st, 2023]]
***

- # Resources
	- [Real world Ocaml](https://dev.realworldocaml.org/platform.html)
	-
- # Setup
	- Installation du langage et du gestionnaire de paquets
		- `sudo pacman -Syu ocaml opam`
	- **Switch** : Environnement avec ces propres dépendances
		- `opam init`
			- Construction du switch par défaut dans `~/.opam/default`
		- `opam switch`
			- Liste les environnements disponibles
		- `opam switch create <path>`
			- Construction d'un nouveau switch
		- Configuration minimal
			- Installer le système de build automatique [Dune](https://dune.build/)
				- `opam install dune dune-release`
			- Génération de documentation et mise en forme
				- `opam install odoc ocamlformat`
			- Interpréteur avancé
				- `opam install utop`
				  id:: 64baa458-6823-4cb0-a185-6da8077e40d4
			- Environnement de développement
				- `opam install merlin ocaml-lsp-server` (*merlin* est utilisé par le serveur LSP)
				-
- # Organisation d'un projet
	- ```text
	  |-- dune-project
	  |-- hello.opam
	  |-- lib
	  |   |-- dune
	  |-- bin
	  |   |-- dune
	  |   `-- main.ml
	  `-- test
	      |-- dune
	      `-- hello.ml
	  ```
-