tags:: Clavier, Trackball, Trackpad, Registre à décalage, QMK, OpenScad
author:: #JeremyBois 
alias:: Echinos
link:: [Github](https://github.com/JeremyBois/Echinos)
[[Apr 8th, 2023]]
***

- ↳ [[Clavier]]
  {{namespace Echinos}}
  ***
- # Tâches
	- DONE Utiliser un câble [[Électronique/Sata]] pour communiquer entre les deux parties
	- DONE Support pour [[Clavier/VIK]] coté clavier
		- The interface includes the following signals (pin 0 to 12)
		      3.3V
		      GND
		      SDA
		      SCL
		      RGB Data Out
		      5V
		      Digital/Analog GPIO 1
		      MOSI
		      Digital/Analog GPIO 2
		      SPI CS
		      MISO
		      SCLK
			- [[Ptechinos]] utilise l'ordre inverse pour être compatible directement avec [[GlidePointCircle]]
				- Possible d'être compatible avec les deux en utilisant un câble inversé
					- Câble normal (type A) **inverse** inverse l'ordre des pistes
					- Câble inversé (Type D) **conserve** l'ordre des pistes
	- DONE Valider l'utilisation d'un oscillateur
		- [Un large nombre de raisons en faveur de l'oscillateur](https://www.sitime.com/top-8-reasons-use-oscillator-instead-crystal-resonator)
	- TODO Détection de l'orientation de l'USB C
		- [TUSB321 (Détecteur)](https://www.ti.com/lit/ds/symlink/tusb321.pdf) + [TPD4E05U06 (protection)](https://www.ti.com/lit/ds/symlink/tpd4e05u06.pdf)
		- Fait par [[Clavier/Honeydew]] mais pourquoi ??
	- DONE Sélection de la diode TVS pour protéger l'USB (5.0V)
		- ~~[TPD2E2U06-Q1](https://www.ti.com/lit/ds/symlink/tpd2e2u06-q1.pdf) (LCSC = C915089, C5350871)~~
			- [SOT 323 (SC70-3, UMT3)](https://en.wikipedia.org/wiki/List_of_integrated_circuit_packaging_types#Small-outline_transistor_(SOT))
		- [ESD7L5.0DT5G-N](https://datasheet.lcsc.com/lcsc/2306211546_BORN-ESD7L5-0DT5G-N_C6165124.pdf)
			- [SOT 723](https://en.wikipedia.org/wiki/List_of_integrated_circuit_packaging_types#Small-outline_transistor_(SOT))
	- DONE Sélection de la diode pour protéger la communication entre les deux parties (3.3V)
		- [D3V3F4U6S](https://www.lcsc.com/product-detail/ESD-Protection-Devices_Diodes-Incorporated-D3V3F4U6S-7_C1869321.html)
			- [SOT-363 (SC-88, SC-70-6)](https://en.wikipedia.org/wiki/List_of_integrated_circuit_packaging_types#Small-outline_transistor_(SOT))
	- DONE Sélectionner la taille de la mémoire flash
		- Notes
			- Max = 16Mo
			- [Footprint compatible 209mil 8-SOP et 8x6mm 8-WSON](https://www.macronix.com/Lists/ApplicationNote/Attachments/2044/AN0226V2%20-%20209mil%208-SOP%20and%208x6mm%208-WSON%20Dual%20Layout%20Guide.pdf)
		- [ZD25WQ32C (4Mo)](https://datasheet.lcsc.com/lcsc/2211091800_Zetta-ZD25WQ32CEIGR_C5258281.pdf)
			- Fonctionne (utilisé pour le [[Clavier/Honeydew]] )
		- [W25Q128JV (16Mo)](https://www.winbond.com/resource-files/w25q128jv_dtr%20revc%2003272018%20plus.pdf)
			- Fonctionne (utilisé sur de nombreux PCB et la documentation officielle)
	- DONE Déterminer les tailles minimales pour les différentes lignes
		- |     Nom    | Power | USB | Signal |
		  |:----------:|:-----:|:---:|--------|
		  | Espacement |  0.2  | 0.15 | 0.15    |
		  | Largeur Min | 0.2 | 0.2 | 0.15  |
		  | Largeur Max | NaN | 0.2 | NaN |
		  | Raison     |  MCU   | Impédance | MCU    |
	- DONE Communication #UART 2 fils entre les deux parties
		- Permet la synchronisation bidirectionnelle avec #KMK
		- Compatible aussi avec #QMK sans être nécessaire
	- TODO Communication #UART 2 fils vers une puce #Bluetooth
		- Communication vers téléphone / autre ordi
		- Doit être possible de basculer entre #Électronique/USB et #Bluetooth
			- #QMK ou #KMK peut le faire ??
	- DONE Encodeur à l'extérieur pour pas géner ??
		- La position actuelle sur #Ptechinos est pas top car je l'active sans le vouloir
		- Voir si c'est toujours le cas avec un espacement MX
	- DONE Utiliser un encodeur [[AlpsAlpine/EC12E]] à la place du [[Panasonic/EVQWGD001]] ???
		- Circulaire
		- low profile
		- perte du clic
	- DONE Empreinte de switch pour #hotswap compatible avec
		- DONE Valider que c'est possible
		- ~~[[Kailh/Choc mini]]~~
		- [[Kailh/Choc V1]]
		- [[Kailh/Choc V2]]
		- [[Gateron/KS33 low profile]]
		- [[Gateron/KS27 low profile]]
		- [[Cherry/MX]]
	- DONE Utiliser un espacement MX
		- DONE Maj sur générateur #OpenScad
		- DONE Maj sur #Kicad
	- DONE Améliorer la position de l'USB et du microcontrolleur
		- USB à gauche au dessus du petit doigt externe
			- Orienté vers le haut si possible
		- Microcontrolleur au centre en bas
			- Au niveau de la paume de la main
		- Libère toute la partie à droite (interne) pour   mettre les modules
			- Pogo + aimants
			- FPC (voir #Clavier/VIK)
	- DONE Améliorer la position du connecteur SATA
		- Doit être en majeure partie sur le PCB
		- Attention à ne pas empêcher
			- l'utilisation du joystick
			- l'utilisation de capuchons en taille 1.5
	- TODO Valider le support pour #Clavier/VIK
		- Ajouter un jumper sur 5V pour être compatible avec le module Cirque en SPI
		- Valider le connecteur sur le clavier
		- Valider le connecteur sur les modules
	- TODO Ajouter les vias vers GND (via stitching)
		- Faire un mur en bordure pour isoler de l'extérieur
			- Signaux externes qui entrent --> parasites
			- Signaux internes qui sortent --> parasites
		- Ajouter des vias sur l'ensemble du PCB
			- Évite les antennes
			- Permet un retour plus rapide du courant --> moins de parasites
			- Meilleure dissipation thermique
	- TODO Ajouter la posibilité de mettre un joystick digital sur le pouce interne
		- Il faut qu'il soit orientable pour être confortable à utiliser
		- Semble complexe de mettre l'empreinte directement sur le PCB principal
			- Utiliser un PCB vertical comme dans la [[Ploopy/Classic]] ou [[Clavier/Generative KAiBoard]]
	- TODO Faire la partie droite
		- Utiliser l'outil de mirroir pour les traces directement depuis PCBnew
		- Faire les empreintes mirroirs depuis l'éditeur d'empreinte
			- Surcharger les empreintes dans le PCB si elles sont génériques
			- Faire des variantes mirroirs pour les composants propres à Echinos
		-
- # Notes
	- Couleurs
		- Theme Zelda a link to the past
			- Base --> vert forêt
			- Finition PCB --> Or / Doré (ENIG)
			- Top plate --> Or / Dorée
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
		- Empreintes pour [[Kailh/Choc V1]] et [[Kailh/Choc mini]]
		- Utiliser des [[Registre à décalage]] ((64282b87-401d-4557-9f0c-7dfb1bf57497)) pour gérer les colonnes
		- Utiliser un [[Waveshare/RP2040 zero]]
			- Prend pas de place
			- Expose de nombreux pins
	- Valider la compatibilité avec #KMK
		- Support filaire et/ou #Bluetooth
		- Modifiable sans recompilation
		- TODO Vérifier que ce n'est pas trop lent
- # Options
  id:: 643164d9-b6fd-4277-8738-969734d6c1a0
	- Voir les modules existants compatibles avec [[Clavier/VIK]]
	- ## Trackball
	  id:: 643164e5-3903-461b-aff9-67821e9128cb
		- Composant [[Pixar/PMW3360DM-T2QU]]
			- Utilisation de ((4d11a85a-63b7-437d-b681-b8b1550b686a))
	- ## Trackpad
	  id:: 643164ec-6f86-4685-9537-a178db9b1195
		- Composant [[Cirque/GlidePointCircle]]
	- ## Encodeur
	  id:: 643164f0-772b-41a5-909e-0525e4fc0b1f
		- Composant [[Panasonic/EVQWGD001]]
	- ## Joystick
	  id:: 6431652d-420c-49e3-bad0-6aab3c916bc8
	- ## LCD / OLED