tags:: #Clavier #CAD #PCB #Projet 
link:: 
[[Feb 23rd, 2023]]

- #+BEGIN_WARNING
  **Document partagé permettant de conserver une trace des nouvelles idées / remarques** 
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
- # Firmware
	- ## Commun
		- Utiliser directement la commande `make` en se plaçant directement dans le dossier  racine --> *qmk_firmware*
			- `make --jobs=1 ptechinos/2040:default trackpad=true`
		- Pour que QMK puisse flasher le microcontrôleur il doit être monté (bootloader mode)
	- ## Trackball
		- TODO [Auto mouse layer](https://github.com/qmk/qmk_firmware/blob/master/docs/feature_pointing_device.md#automatic-mouse-layer-idpointing-device-auto-mouse)
		- Build pour la trackball
			- **EE_HANDS**
				- `make --jobs=1 ptechinos/2040:default:uf2-split-right trackball=true`
			- **#define MASTER_RIGHT**
				- `make --jobs=1 ptechinos/2040:default trackball=true`
	- ## Trackpad
		- TODO [Auto mouse layer](https://github.com/qmk/qmk_firmware/blob/master/docs/feature_pointing_device.md#automatic-mouse-layer-idpointing-device-auto-mouse)