type:: [[Book]]
author:: #[[Tony R. Kuphaldt]]
tags:: Électronique, Formation
link:: [PDF (original)](http://www.ibiblio.org/kuphaldt/electricCircuits/DC/index.html)  [Online (All about circuit)](https://www.allaboutcircuits.com/textbook/direct-current/)
[[Jul 10th, 2023]]
***

- ## Concepts de base en électricité
	- link:: [Basic concepts of electricity](https://www.allaboutcircuits.com/textbook/direct-current/chpt-1)
	- La **tension** ($V$, volt) est la mesure de l'énergie potentielle relative par charge unitaire
		- Elle se mesure entre deux points
		- Le signe est fonction du sens de circulation et de l'ordre des points choisi
	- Le courant ($A$, ampère) est la mesure de l'intensité du circuit
		- Il se mesure en un point du circuit
		- Mesure de la vitesse de déplacement des charges à travers le circuit
	- Sens de circulation des électrons
		- Sens physique
		- Du - vers le +
			- Le - représente un surplus d'électrons
				- Charge négative
			- Le + représente un déficit d'électrons
				- Charge positive
	- Sens de circulation conventionel
	  id:: 64ac7354-44a3-4bf2-ac86-2c911dc4651a
		- Sens courant / historique
		- Du + vers le -
			- Le + représente un surplus de charge
				- Nombre d'électrons **plus** important
			- Le - représente un déficit de charge
				- Nombre d'électrons **moins** important
	- Polarité
		- Un composant polarisé n'a pas le même comportement suivant le sens du courant
		  collapsed:: true
			- Diode, batterie, ...
			- Le symbole contient une flèche indiquant le ((64ac7354-44a3-4bf2-ac86-2c911dc4651a))
		- Un composant non polarisé a le même comportement dans les deux sens
		  collapsed:: true
			- Résistance, condensateur, ...
- ## Loi d'Ohm
	- link:: [Ohm's law](https://www.allaboutcircuits.com/textbook/direct-current/chpt-2/)
	- La résistance (R en $Ω$) est la mesure relative de l'opposition au mouvement du flux
		- Se mesure entre deux points
		- ![Symbole résistance (zigzag)](https://www.allaboutcircuits.com/uploads/articles/resistor-symbol-zig-zag.jpg) ![Symbole résistance (rectangle)](https://www.allaboutcircuits.com/uploads/articles/rectangular-box-resistor-schematic-symbol.jpg)
	- ![U_R_I](https://www.allaboutcircuits.com/uploads/articles/units-measurement-electrical-current.png)
		- $E = R \times I$
			- Majuscule pour une valeur continue
			- Minuscule pour une valeur instantanée
	- La puissance ($P$, watt) est la mesure du travail sur une période de temps
		- Loi d'Ohm
			- $P = I \times E$
		- Loi de Joules
			- $P = I^2 \times R$
			- $P = \frac{E^2}{R}$
	- Un symbôle avec une flèche en diagonal sert à indiquer une valeur variable
		- ![Symbole résitance variable](https://www.allaboutcircuits.com/uploads/articles/variable-resistance-resistors.jpg)
	- Une résistance a une limite de dissipation thermique (en watt)
		- Fortement dépendante de sa taille
		- À calculer en fonction du courant / tension
	- La résistance varie avec la température et la loi d'ohm n'est donc qu'une approximation théorique
		- Non linéarité de la valeur de résistance
		- Certains composants / matériaux ont une résistance qui diminue pour une certaine plage de tension
			- ![region négative résistance](https://www.allaboutcircuits.com/uploads/articles/region-of-negative-resistance.jpg)
			- Tetrode tube, Esaki, tunnel diode, ...
	- Deux points d'un circuit sont communs si la résistance entre est négligeable
		- Tension nulle entre deux points dits communs
		- Résistance des fils négligeable dans la plupart des cas
		-
- DOING Sécurité électrique
	- link:: [Electrical safety](https://www.allaboutcircuits.com/textbook/direct-current/chpt-3)
	-