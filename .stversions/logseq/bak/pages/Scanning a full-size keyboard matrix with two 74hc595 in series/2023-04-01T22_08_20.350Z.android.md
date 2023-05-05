type:: [[Article]]
author:: #Mehmedbasic
tags:: Hardware, Software, QMK, ShiftRegister
link:: https://mehmedbasic.dk/post/74hc595-keyboard/
[[Apr 1st, 2023]]

- Comment utiliser des registres à décalage pour permettre de faire le scan de l'ensemble des touches d'un clavier avec seulement 3 pins
  id:: 642828da-1be8-49df-9f23-672e301f811c
- # Problèmes
	- Le nombre de pins sur les microcontrolleurs est limité
- # Solution
	- Utiliser un registre à décalage ((64282b87-401d-4557-9f0c-7dfb1bf57497))
		- Modèle *74hc595* (active high)
		- Très très rapide (20MHz)