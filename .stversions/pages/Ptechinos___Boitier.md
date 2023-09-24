tags:: Ergonomie, Clavier, CAD
[[Sep 20th, 2023]]
***

- ↳ [[Ptechinos]] 
  ***
- # Tâches
	- DOING Réduire l'espace entre le bas du boitier et le PCB
		- Espace inutile voir négatif pour la qualité sonore
		- **Réduction de 1mm**
			- Potentiellement nécessaire d'abaisser les support prévues pour les entretoises
			- Ajuster l'ouverture des deux pogos
	- TODO Tenir compte de la sur-élévation des switch au niveau de la top plate
		- Switch ~0.5mm plus haut
		- Pas forcément nécessaire comme on abaisse le PCB de 1mm
	- DOING Prévoir un trou / cassure dans la bordure pour supporter le PCB
		- Nécessaire pour laisser la place pour le hotswap
			- Pouce intérieur
			- Pouce intérieur
			- Petit doigt extérieur
	- DONE Placer correctement les trous pour les têtes de vis au niveau de la top plate
	- DOING Augmenter la hauteur des trous pour les aimants
		- 0.1mm devrait suffire pour éviter aux aimants de dépasser
- ***
- # Description
- ## Isolation phonique
	- #+BEGIN_NOTE
	  Élévation / réduction est notée `<valeur` pour indiquer que le tassement entre aussi en jeu
	  #+END_NOTE
	- Pad en Poron de 0.5mm entre PCB et switch
		- Réduit le bruit
		- Améliore la stabilité du switch
			- Moins de vibrations
		- Sur-élève le switch de <0.5mm
			- Entraîne la sur-élévation du capuchon aussi
		- Ne change pas la course
		- TODO Ajouter référence
	- Scotch à l'intérieur des switch aux points de contact entre mécanisme et boitier
		- Réduit fortement le bruit lors du relachement de la touche
		- TODO Ajouter lien vidéo
	- Lubrification des zones de frottements dans le switch
		- Linéarisation de la course
		- Réduction de la vitesse de retour après relachement de la touche
		- Réduction des bruits parasitaires
		- TODO Ajouter référence
	- Pad en EVA de 1mm entre capuchon et switch
		- Réduit la course du switch de <1mm
		- Sur-élève le capuchon de <1mm
			- La hauteur du switch reste elle identique
		- TODO Ajouter référence
	- Mousse EVA de 2mm sous le PCB
		- Réduit la caisse de résonnance
		- Pas d'impact sur la hauteur finale
		- TODO Ajouter référence