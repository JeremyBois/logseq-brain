tags:: Functional, OOP
alias:: Ocaml
link:: https://ocaml.org/ 
[[Jul 21st, 2023]]
***

- # Resources
	- [Real world Ocaml](https://dev.realworldocaml.org/platform.html)
	-
- # Setup
	- Installer le langage et le gestionnaire de paquets
		- `sudo pacman -Syu ocaml opam`
	- Construire un environnement avec ces propres dépendances --> **Switch**
		- `opam init` construit un **switch** par défaut dans `~/.opam/default`
	- Voir les **switch** existants
		- `opam switch`
	- Installer un système de build automatique
		- `opam tdune dune-release`
	- Génération de documentation et mise en forme
		- `opam odoc ocamlformat`
	- Interpréteur avancé
		- `opam utop`
		  id:: 64baa458-6823-4cb0-a185-6da8077e40d4
		-