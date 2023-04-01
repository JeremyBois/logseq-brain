tags:: Hardware, Software
alias:: ShiftRegister ShiftRegisters, Registres à décalage
link:: [Wikipédia](https://en.wikipedia.org/wiki/Shift_register)
title:: Registre à décalage
[[Apr 1st, 2023]]

- # Principe
	- Composant constitué de [[bascules]] connectées en cascade
		- Horloges partagées
			- Selon les modèles on peut avoir plusieurs horloges pour contrôler
				- entrées vers mémoire
				- mémoire vers sorties
		- Valeur stockée transmise d'une bascule à l'autre à chaque tick de l'horloge
			- La sortie de la bascule *n* est l'entrée de la bascule *n+1*
		- Valeurs en entrées stockées en mémoire
			- Mise à jour uniquement à chaque tick de l'horloge
		- Valeurs en mémoire transmises en sortie
			- Mise à jour uniquement à chaque tick de l'horloge
	- Chaque registre peut être connecté en série à un autre registre afin de multiplier les entrées et/ou sorties
	- ## Variantes
		- **Serial in - Serial out (SISO)**
			- Permet de transmettre un [[bit]] d'une entrée vers une sortie
				- La valeur en entrée est transmise en sortie à chaque tick de l'horloge
		- **Serial in - Parallel out (SIPO)**
		  id:: 64282b87-401d-4557-9f0c-7dfb1bf57497
			- Permet de transmettre un [[Byte]] d'une entrée vers plusieurs sorties
				- La valeur en entrée est envoyée séquentiellement aux sorties à chaque tick de l'horloge
			- Permet dé-multiplier une sortie vers *x* sorties
				- Revient à déconstruire un byte (entrée) en bits (sorties)
		- **Parallel in - Serial out (PISO)**
			- Permet de transmettre plusieurs bits en entrée séquenciellement vers une unique sortie
				- Chaque tick de l'horloge permet de lire la valeur associée à une entrée
			- Permet de regrouper plusieurs entrées sur une même entrée
				- Reconstruire un byte (sortie) représentant l'état des différentes bits (entrées)
		- **Parallel in - Parallel out (PIPO)**
			- Permet de transmettre bit par bit les entrées et de les lire bit par bit en sortie
				- Chaque tick de l'horloge permet le transfert de toutes les entrées vers les sorties
		- **Universel**
			- Un unique composant supportant les différentes variantes
	- ## Types
		- ### Set Reset latches
			- Utilise des portes logiques *NOR*
			- **Active low**
				- Dans l'état de repos les
		- **Active high**
		-
- # Connections
	- [[Scanning a full-size keyboard matrix with two 74hc595 in series]]
		- {{embed ((642828da-1be8-49df-9f23-672e301f811c))}}
	- [[The Learning Circuit/How Shift Registers Work]]
	- [[The Learning Circuit/How to Add Outputs to an Arduino using a Shift Register]]
	- [[The Learning Circuit/How to Add Multiple Inputs to an Arduino using a Shift Register]]