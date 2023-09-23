tags:: Clavier, Trackball, Trackpad, Registre à décalage, QMK, OpenScad
author:: #JeremyBois 
alias:: Echinos
link:: [Github](https://github.com/JeremyBois/Echinos)
[[Apr 8th, 2023]]

-
- # Tâches
	- TODO Support pour [[Clavier/VIK]]
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
	- TODO Valider l'utilisation d'un oscillateur
		- [Un large nombre de raisons en faveur de l'oscillateur](https://www.sitime.com/top-8-reasons-use-oscillator-instead-crystal-resonator)
	- TODO Détection de l'orientation de l'USB C
		- [TUSB321 (Détecteur)](https://www.ti.com/lit/ds/symlink/tusb321.pdf) + [TPD4E05U06 (protection)](https://www.ti.com/lit/ds/symlink/tpd4e05u06.pdf)
		- Fait par [[Clavier/Honeydew]] mais pourquoi ??
	- TODO Sélection de la diode TVS pour protéger l'USB
		- [TPD2E2U06-Q1](https://www.ti.com/lit/ds/symlink/tpd2e2u06-q1.pdf) (LCSC = C915089, C5350871)
			- [SOT 323 (SC70-3, UMT3)](https://en.wikipedia.org/wiki/List_of_integrated_circuit_packaging_types#Small-outline_transistor_(SOT))
		- [ESD7L5.0DT5G-N](https://datasheet.lcsc.com/lcsc/2306211546_BORN-ESD7L5-0DT5G-N_C6165124.pdf)
			- [SOT 723](https://en.wikipedia.org/wiki/List_of_integrated_circuit_packaging_types#Small-outline_transistor_(SOT))
	- TODO Sélectionner la taille de la mémoire flash
		- Notes
			- Max = 16Mo
			- [Footprint compatible 209mil 8-SOP et 8x6mm 8-WSON](https://www.macronix.com/Lists/ApplicationNote/Attachments/2044/AN0226V2%20-%20209mil%208-SOP%20and%208x6mm%208-WSON%20Dual%20Layout%20Guide.pdf)
		- [ZD25WQ32C (4Mo)](https://datasheet.lcsc.com/lcsc/2211091800_Zetta-ZD25WQ32CEIGR_C5258281.pdf)
			- Fonctionne (utilisé pour le [[Clavier/Honeydew]] )
		- [W25Q128JV (16Mo)](https://www.winbond.com/resource-files/w25q128jv_dtr%20revc%2003272018%20plus.pdf)
			- Fonctionne (utilisé sur de nombreux PCB et la documentation officielle)
	- TODO Déterminer les tailles minimales pour les différentes lignes
		- |     Nom    | Power | USB | Signal |
		  |:----------:|:-----:|:---:|--------|
		  | Espacement |  0.2  | 0.2 | 0.2    |
		  |  Largeur | 0.254 | 0.3 | 0.254  |
		  | Raison     |  MCU   | USB | MCU    |
	- TODO Communication #UART 2 fils entre les deux parties
		- Permet la synchronisation bidirectionnelle avec #KMK
		- Compatible aussi avec #QMK sans être nécessaire
	- TODO Communication #UART 2 fils vers une puce #Bluetooth
		- Communication vers téléphone / autre ordi
		- Doit être possible de basculer entre #USB et #Bluetooth
			- #QMK ou #KMK peut le faire ??
	- TODO Encodeur à l'extérieur pour pas géner ??
	- TODO Empreinte compatible avec
		- [[Électronique/Choc mini]]
		- [[Électronique/Choc]]
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
		- Empreintes pour [[Électronique/Choc]] et [[Électronique/Choc mini]]
		- Utiliser des [[Registre à décalage]] ((64282b87-401d-4557-9f0c-7dfb1bf57497)) pour gérer les colonnes
		- Utiliser un [[Électronique/RP2040 zero]]
			- Prend pas de place
			- Expose de nombreux pins
	- Valider la compatibilité avec #KMK
		- Support filaire et/ou #Bluetooth
		- Modifiable sans recompilation
		- TODO Vérifier que ce n'est pas trop lent
- # Options
  id:: 643164d9-b6fd-4277-8738-969734d6c1a0
	- ## Trackball
	  id:: 643164e5-3903-461b-aff9-67821e9128cb
		- Composant [[Électronique/PMW3360DM-T2QU]]
			- Utilisation de ((4d11a85a-63b7-437d-b681-b8b1550b686a))
		- DONE Refaire le PCB pour le capteur
			- [Ogen](https://github.com/JeremyBois/Ogen) n'a pas de distinction de voltage sur les différents VDD alors qu'il faudrait du 3.3V et du 1.9V pour être cohérent
			- Régulateurs de courant
				- Sortie ajustable
					- [AP2127K-ADJTRG1](https://www.lcsc.com/product-detail/Linear-Voltage-Regulators-LDO_Diodes-Incorporated-AP2127K-ADJTRG1_C96343.html)
						- Nécessite 2 résistances pour fixer la tension de sortie
				- Sortie fixe :
					- --> 1.9V [VRH1902LTX](https://www.lcsc.com/product-detail/Linear-Voltage-Regulators-LDO_AnaSem-VRH1902LTX_C697975.html)
					- --> 3.3V [AP2127K-3-3TRG1](https://www.lcsc.com/product-detail/Linear-Voltage-Regulators-LDO_Diodes-Incorporated-AP2127K-3-3TRG1_C156285.html)
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