type:: [[Article]]
author:: #Mehmedbasic
tags:: Hardware, Software, QMK, ShiftRegister
link:: https://mehmedbasic.dk/post/74hc595-keyboard/
[[Apr 1st, 2023]]

- Comment utiliser des registres à décalage pour permettre de faire le scan de l'ensemble des touches d'un clavier
  id:: 642828da-1be8-49df-9f23-672e301f811c
- # Problèmes
	- Le nombre de pins sur les microcontrolleurs est limité
- # Solution
	- Colonnes
		- Utiliser un [[Registre à décalage]] ((64282b87-401d-4557-9f0c-7dfb1bf57497))
			- Modèle *74hc595*
				- Utilise des bascules ((64289d37-3c2a-4f0d-bee6-9dc4bca1d209))
				- {{embed ((64289354-60ce-4bbb-a17e-7cfbe5e8894f))}}
			- Très très rapide (20MHz)
	- Lignes
		- Utiliser un pin par ligne
		- Trop peu de lignes pour rentabiliser l'utilisation d'un [[Registre à décalage]]