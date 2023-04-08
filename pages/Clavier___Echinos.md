tags:: Clavier, Trackball, Trackpad, Registre à décalage, QMK, OpenScad
alias:: Echinos
link::
[[Apr 8th, 2023]]

- # Développement
	- Combiner 3D et électronique pour obtenir un boitier adapté et limiter la complexité liée au processus itératif
	- 3D / 2D --> #OpenScad
		- Utiliser une projection du boitier sur le plan (XY) comme base pour le positionnement des  composants
			- Permet de s'assurer que le boitier est compatible
			- Permet d'avoir un processus itératif linéaire entre électronique et 3D
		- Le boitier ne doit pas être dépendant des composants
			- Évite l'effet yoyo quand on veut modifier la position des switches
	- Électronique --> #Kicad
		- #PCB non réversible
		- Empreintes pour [[Capuchon/Choc]] et [[Capuchon/Choc mini]]
		-
- # Options
	- ## Trackball
		- Composant [[Electronique/PMW3360DM-T2QU]]
			- Utilisation de ((4d11a85a-63b7-437d-b681-b8b1550b686a))
	- ## Trackpad
		- Composant [[Electronique/GlidePointCircle]]
	- ## Encodeur
		- Composant [[Electronique/EVQWGD001]]
	- ## Joystick
	- ## LCD / OLED
	-
	-