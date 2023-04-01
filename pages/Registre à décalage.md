tags:: Hardware, Software
alias:: ShiftRegister ShiftRegisters, Registres à décalage
link:: [Wikipédia](https://en.wikipedia.org/wiki/Shift_register)
title:: Registre à décalage
[[Apr 1st, 2023]]

-
- # Principe
	- Composant constitué de [[Bascules]] connectées en cascade
		- Horloge partagée
		- Valeur stockée transmise d'une bascule à l'autre à chaque tick de l'horloge
			- La sortie de la bascule *n* est l'entrée de la bascule *n+1*
	- Plusieurs variantes
		- Serial in - Serial out (SISO)
			- Permet de transmettre bit par bit à plusieurs sortie
		- Serial in - Parallel out (SIPO)
			- Permet de transmettre un [[byte]] bit par bit à plusieurs sortie
			- Permet d'envoyer un bit à chaque sortie une par une
				- Chaque tick de l'horloge permet d'envoyer un bit
		- Parallel in - Serial out (PISO)
			- Permet d'envoyer / stocker plusieurs bit en entrée et de les lire de manière séquencielle sur la sortie
				- Chaque tick de l'horloge permet de lire la valeur associée à une entrée
				- Permet de reconstruire un [[byte]] représentant l'état des différentes entrées
		- Parallel in - Parallel out (PIPO)
			- Permet d'envoyer bit par bit les entrées et de les lire
	- Permet de multiplier le nombre de
- # Connections
	- [[Scanning a full-size keyboard matrix with two 74hc595 in series]]
		- {{embed ((642828da-1be8-49df-9f23-672e301f811c))}}
	-