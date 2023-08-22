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
- Lambda
	- `\arg1 arg2 -> arg1 <> " " <> arg2`
		- `\`
		- Paramètres
		- `->`
		- Corps de la fonction
	- Permet l'écriture de fonction inline / anonyme
- Opérateur d'application de fonction: `$`
	- ```haskell
	  ($) :: (a -> b) -> a -> b
	  f $ x = f x
	  ```
	- Permet de réduire l'utilisation de parenthèses
- Opérateur de composition de fonction: ` . `
	- ```haskell
	  (.) :: (b -> c) -> (a -> b) -> a -> c
	  f . g = \arg -> f (g arg)
	  ```
	- Permet de chaîner l'application de fonctions
		- Le sortie de la première fonction (`a->b`) est utilisée comme entré de la seconde (`b->c`)
- Infixit
