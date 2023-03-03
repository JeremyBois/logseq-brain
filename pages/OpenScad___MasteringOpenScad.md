type:: [[Book]]
author:: #[[Jochen Kerdels]]
tags:: #OpenScad #CAD #Formation 
link:: https://mastering-openscad.eu/buch/introduction/
[[Mar 3rd, 2023]]

- # Introduction
- Disponible en version papier sur [Amazon](https://www.amazon.com/dp/3753458589)
- Apprentissage à travers 10 projets de plus en plus complexe
- # Généralités
	- https://mastering-openscad.eu/buch/gui-overview/
	- ![UI](https://mastering-openscad.eu/gui-overview-images/overview.png)
		- 1 --> Zone de code
		- 2 --> aperçu et rendu 3d
			- **Preview** pour voir un aperçu rapide
			- **Render** pour générer un rendu final exportable
		- 3 --> Console affichant les erreurs et autre informations
		- 4 --> (Avancé) Customisation / UI en lien avec certaines variables du code
- # Options basiques
	- https://mastering-openscad.eu/buch/basic_ops_and_structure/
	- Le langage utilisé est **descriptif**
		- Ce n'est **pas** un langage de [[Programmation]]
		- Décrit la géométrie à partir de primitives et instructions simples
	- `sphere(r=10);`
		- Indique qu'il existe une primitive sphère avec un rayon de 10mm
	- ```closure
	  radius_with_a_name = 10;
	  sphere( r = radius_with_a_name );
	  radius_with_a_name = 20;
	  ```
		- Indique qu'il existe une variable `radius_with_a_name` ayant pour valeur 20
		- #+BEGIN_CAUTION
		  L'ordre de déclaration n'a pas d'importance.
		  #+END_CAUTION
	- collapsed:: true
	  ```closure
	  adjustment = 0.7;
	  adjustment_factor = 1.05;
	  
	  function adjust(x) = (x + adjustment) * adjustment_factor;
	  
	  main_radius = adjust(10);
	  margin = adjust( 5);
	  depth = adjust(25);
	  ```
		- Possible d'utiliser des **fonctions** pour éviter les répétitions
-