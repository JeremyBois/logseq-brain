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
		- Serial in - Parallel out (SIPO)
			- Permet de transmettre un bit à chaque
		- Parallel in - Serial out (PISO)
			- Permet de regrouper plusieurs entrées sur un même pin
		- Parallel in - Parallel out (PIPO)
	- Permet de multiplier le nombre de
- # Connections
	- [[Scanning a full-size keyboard matrix with two 74hc595 in series]]
		- {{embed ((642828da-1be8-49df-9f23-672e301f811c))}}
	-