tags:: PCB
alias:: Électronique/Noyau de ferrite, Noyau de ferrite, Ferrite bead
link:: [All about circuits](Choosing and Using Ferrite Beads) [Analogue dialogue](https://www.analog.com/en/analog-dialogue/articles/ferrite-beads-demystified.html) [MicroType engineering](https://www.youtube.com/shorts/SApjHiu8eoo)
[[Jul 8th, 2023]]
***

- ## Utilisation
	- Filtrer / limiter les hautes fréquences sur la ligne d'alimentation
	- Isoler les hautes fréquences sur les lignes partagées (analogues et digitales)
- ## Principe
	- Se place en série
	- Trois zones de réponse
		- Inductive ($R < X$)
			- Peut être responsable de la résonnance pallier grâce à des condensateurs en amont et en aval
		- Résistive ($R > X$)
			- Zone dans laquelle doivent se trouver les fréquences a filtrer
			- Agit comme une résistance et dissipe l'énergie sous forme de chaleur
		- Capacitive ($R < X$ après la zone résistive)
			- Ne filtre plus rien
		- ![FerriteBead_ZoneReponse](https://www.analog.com/-/media/images/analog-dialogue/en/volume-50/number-1/articles/ferrite-beads-demystified/ferrite-beads-fig01.png?la=en&imgver=1){:height 249, :width 560}
			- Z est [l'impédance totale](https://fr.wikipedia.org/wiki/Imp%C3%A9dance_(%C3%A9lectricit%C3%A9))
			- R est la [résistance](https://fr.wikipedia.org/wiki/R%C3%A9sistance_(%C3%A9lectricit%C3%A9))
			- X est la [réactance](https://fr.wikipedia.org/wiki/R%C3%A9actance_(%C3%A9lectricit%C3%A9))
		- #+BEGIN_CAUTION
		  Les zones de réponse sont souvent indiquées pour un courant continue nul alors que la variation du courant influe fortement sur le comportement du composant
		  #+END_CAUTION
			- Réduction de l;
			-
- ## Comment la sélectionner ?
	- Courant maximal supporté (*Rated current*)
		- ![FerriteBead_RatedCurrent](https://www.allaboutcircuits.com/uploads/articles/CP4_Wurth_derating.JPG){:height 236, :width 276}
		- Le courant maximal dans le circuit doit correspondre à 20 / 30% du *Rated current* de la noyau de ferrite pour pallier le