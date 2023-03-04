type:: [[Book]]
author:: #[[Jochen Kerdels]]
tags:: #OpenScad #CAD #Formation 
link:: https://mastering-openscad.eu/buch/introduction/
[[Mar 3rd, 2023]]

- # Introduction
- Disponible en version papier sur [Amazon](https://www.amazon.com/dp/3753458589)
- Apprentissage à travers 10 projets de plus en plus complexe
- # Généralités
	- [Source](https://mastering-openscad.eu/buch/gui-overview/)
	- ![overviewOpenscad.png](../assets/overviewOpenscad_1677872956181_0.png){:height 400, :width 607}
		- 1 --> Zone de code
		- 2 --> aperçu et rendu 3d
			- **Preview** pour voir un aperçu rapide
			- **Render** pour générer un rendu final exportable
				-
		- 3 --> Console affichant les erreurs et autre informations
		- 4 --> (Avancé) Customisation / UI en lien avec certaines variables du code
- # Options basiques
	- [Source](https://mastering-openscad.eu/buch/basic_ops_and_structure/)
	- Le langage utilisé est **descriptif**
		- Ce n'est **pas** un langage de [[Programmation]]
		- Décrit la géométrie à partir de primitives et instructions simples
	- L'ordre de déclaration des variables n'a pas d'importance
		- ```openscad
		  radius_with_a_name = 10;
		  sphere( r = radius_with_a_name );
		  radius_with_a_name = 20;
		  ```
			- Il existe une variable `radius_with_a_name` ayant pour valeur 20
				- Seule la dernière valeur est conservée
	- Possible d'utiliser des **fonctions** pour éviter les répétitions
		- ```openscad
		  adjustment = 0.7;
		  adjustment_factor = 1.05;
		  
		  function adjust(x) = (x + adjustment) * adjustment_factor;
		  
		  main_radius = adjust(10);
		  margin = adjust( 5);
		  depth = adjust(25);
		  ```
	- ## Transformations
	- Sytème de coordonnées
		- X = Positif vers l'avant
		- Y = Positif vers la droite
		- Z = Positif vers le haut
		- [[draws/2023-03-03-21-08-29.excalidraw]]
	- Les transformations se font par rapport à l'origine
		- ```openscad
		  rotate( [0,0,45] ) translate( [20,0,0] ) cube(10,true);
		  ```
		- Possible de cumuler des opérations afin de former une nouvelle géométrie
			- L'ordre des transformations est important
	- ## Combining Geometries
-