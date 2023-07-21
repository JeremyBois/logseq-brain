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
	- Construire un environnement avec ces propres dépendances --> **Switch**
		- `opam init` construit un **switch** par défaut dans `~/.opam/default`
			- `opam switch` pour voir les **switch** disponibles sur son ordinateur
			- opam switch create <path>` pour construire un nouveau **switch**
	- Configuration d'un **switch**
		- Installer un système de build automatique
			- `opam install tdune dune-release`
		- Génération de documentation et mise en forme
			- `opam install odoc ocamlformat`
		- Interpréteur avancé
			- `opam install utop`
			  id:: 64baa458-6823-4cb0-a185-6da8077e40d4
		- Environnement de développement
			- `opam install merlin ocaml-lsp-server` (*merlin* est utilisé par le serveur LSP)
			-
			-