tags:: #Clavier #CAD #PCB #Projet 
link:: 
[[Feb 23rd, 2023]]

- #+BEGIN_WARNING
  **Document partagé entre les différents claviers**
  #+END_WARNING
- # Boitier
	- ## Fixation sandwich (plaques entre elles)
		- Utiliser des aimants pour faire tenir les différentes plates entre elles
			- Épaisseur des aimants pour **rigidifier** l'ensemble #PCB / `top plate`
				- Éviter que la `top plate` se déclipse
				- Éviter de voir la tête de vis dépasser
			- Simplifie l'assemblage et la maintenance
		- Utiliser des vis / entretoise en nilon en taille **M3**
			- Tête de vis au dessus du #PCB et fixé dans le boitier suivant deux options :
				- Entretoise directement dans le modèle 3D du boitier
					- Aspect monobloc non dépendant de pièces externes
				- Entretoise collée sur le fond du boitier
					- Permet de simplifier la réparation si besoin par la suite
					- Nécessite des entretoises externes
			- Épaisseur de la tête pour **rigidifier** l'ensemble #PCB / `top plate`
				- Éviter que la `top plate` se déclipse
				- Éviter de voir la tête de vis dépasser
	- Laisser plus de place sur la *top plate* au niveau des encodeurs
		- Permet de laisser passer les switches qui doivent êtres soudés
- # Firmware
	- ## Commun
		- Flasher --> `qmk flash`
			- Promicro
				- Directement possible
			- RP2040
				- Basculer le clavier en mode *bootloader*
				- Monter le clavier comme un disque dur
		- Compilation customisable :
			- Utiliser l'option `-n` pour afficher la commande #Make correspondante utilisable comme base
				- `qmk compile -kb ptechinos/2040 -km default -n` --> `make --jobs=1 ptechinos/2040:default`
			- Utiliser directement la commande `make` en se plaçant directement dans le dossier  racine (*qmk_firmware*)
			- **EE_HANDS**
				- `make --jobs=1 ptechinos/2040:default:uf2-split-right trackball=true`
				- `make --jobs=1 ptechinos/2040:default:uf2-split-left trackpad=true`
			- **#define MASTER_RIGHT**
				- `make --jobs=1 ptechinos/2040:default trackball=true`
			- **#define MASTER_LEFT**
				- `make --jobs=1 ptechinos/2040:default trackpad=true`
	- [Auto mouse layer](https://github.com/qmk/qmk_firmware/blob/master/docs/feature_pointing_device.md#automatic-mouse-layer-idpointing-device-auto-mouse)
		- Permet d'activer une couche quand on utilise le #Trackpad ou la #Trackball
		- Permet de d'ajouter les clics de souris ou autres outils de navigation
- # Layout
	- *Shift* avec ((640bbca1-3642-48bf-a8a9-57c18d9f0ea3))
		- Gauche --> `S+F`
		- Droite    --> `J+L`
		- Avantages :
			- Éviter un *mod tap*
			- Réduit l'utilisation du petit doigt
			- Simplifier la navigation
				- Debug #Unity
				- Jeux
			- Force l'utilisation des deux mains
	- ## Combos
	  id:: 640bbca1-3642-48bf-a8a9-57c18d9f0ea3
		- Combiner plusieurs touches en même temps
		- Ressources
			- [Combos pour les modificateurs](https://jasoncarloscox.com/blog/combo-mods/)
- # Trackball
	- DOING Souder le pont JP1 pour ajouter la ((64287c00-cf70-4201-b24f-a0efe78451bb)) sur la ligne MISO
		- [Github Ogen PCB](https://github.com/JeremyBois/Ogen)
		- [MISO peut être flottant car contrôlée par l'esclave uniquement](https://electronics.stackexchange.com/a/234707)