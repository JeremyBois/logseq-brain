id:: 64c0f88e-f83e-4b43-b417-aa0897dfdd5f
type:: [[Book]]
author:: #[[Rebecca Skinner]]
tags:: Haskell
parent:: Haskell
link:: https://pragprog.com/titles/rshaskell/effective-haskell/
***

- ![Viewer](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf) | [PDF](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
  ↳ [Notes]([[hls__Effective-Haskell_P1.0_1691935393283_0]])
  ***
- Approche du langage avec des applications
-
- Lambda
	- `\arg1 arg2 -> arg1 <> " " <> arg2`
		- `\`
		- Paramètres
		- `->`
		- Corps de la fonction
- Opérateur d'application de fonction
	- `$`
	- `(a -> b) -> a -> b`
	- Permet de réduire l'utilisation de parenthèses
- Opérateur de composition de fonction
	- ` . `
	- `(b -> c) -> (a -> b) -> a -> c`
	- Permet de chaîner l'application de fonctions
		- Le sortie de la première fonction (`a->b`) est utilisée comme entré de la seconde (b->c)
-