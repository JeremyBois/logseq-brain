tags:: Clavier, Trackball, Trackpad, Registre à décalage, QMK, OpenScad
alias:: Echinos
link::
[[Apr 8th, 2023]]

- # Développement
	- Combiner 3D et électronique pour obtenir un boitier adapté et limiter la complexité liée au processus itératif
	- Support de nombreuses ((643164d9-b6fd-4277-8738-969734d6c1a0))
	- 3D / 2D --> #OpenScad
		- Utiliser une projection du boitier sur le plan (XY) comme base pour le positionnement des  composants
			- Permet de s'assurer que le boitier est compatible
			- Permet d'avoir un processus itératif linéaire entre électronique et 3D
		- Le boitier ne doit pas être dépendant des composants
			- Évite l'effet yoyo quand on veut modifier la position des switches
	- Électronique --> #Kicad
		- #PCB non **réversible** mais **symmétrique**
		- Empreintes pour [[Électronique/Choc]] et [[Électronique/Choc mini]]
		- Utiliser des [[Registre à décalage]] ((64282b87-401d-4557-9f0c-7dfb1bf57497)) pour gérer les colonnes
		- Utiliser un [[Électronique/RP2040 zero]]
			- Prend pas de place
			- Expose de nombreux pins
- # Options
  id:: 643164d9-b6fd-4277-8738-969734d6c1a0
	- ## Trackball
	  id:: 643164e5-3903-461b-aff9-67821e9128cb
		- Composant [[Électronique/PMW3360DM-T2QU]]
			- Utilisation de ((4d11a85a-63b7-437d-b681-b8b1550b686a))
	- ## Trackpad
	  id:: 643164ec-6f86-4685-9537-a178db9b1195
		- Composant [[Électronique/GlidePointCircle]]
	- ## Encodeur
	  id:: 643164f0-772b-41a5-909e-0525e4fc0b1f
		- Composant [[Électronique/EVQWGD001]]
	- ## Joystick
	  id:: 6431652d-420c-49e3-bad0-6aab3c916bc8
	- ## LCD / OLED
	-
	-