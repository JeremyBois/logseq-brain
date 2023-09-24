tags:: Clavier, PCB, QMK, Kicad
link:: [Github](https://github.com/JeremyBois/qmk-ptechinos)
[[Sep 24th, 2023]]
***

- ↳ [[Ptechinos]]
  ***
- ## Mise à jour
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