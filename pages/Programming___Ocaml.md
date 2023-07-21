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
		- `opam init` puis `eval $(opam env)`
			- Construction du switch par défaut dans `~/.opam/default`
			- Charger directement ce switch dans chaque shell en modifiant le `.bashrc` avec
				- ```bash
				  ### Opam
				  test -r /home/pampi/.opam/opam-init/init.sh && . /home/pampi/.opam/opam-init/init.sh > /dev/null 2> /dev/null || true
				  ```
		- `opam switch`
			- Liste les environnements disponibles
		- `opam switch create <path>` puis `eval $(opam env)`
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
	- **LSP**
		- ```json
		  "ocaml": {
		      "command": [
		          "/home/pampi/.opam/default/bin/ocamllsp",
		          "--stdio"
		      ],
		      "env": {
		          "PATH": "$PATH:/home/pampi/.opam/default/bin/"
		      },
		      "selector": "source.reason | source.ocaml",
		  },
		  ```
		- Par défaut le serveur récupère uniquement les informations à partir du dernier build
			- Si le projet utilise Dune  on peut maintenir à jour les informations de build automatiquement
				- `dune build -w` ou `dune build --watch`
			- Plus d'informations dans la [documentation](https://github.com/ocaml/ocaml-lsp#usage))
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