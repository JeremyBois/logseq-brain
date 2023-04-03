tags:: Harware, Software
alias:: Résistances, Resistor, Resistors 
link:: [Wikipédia](https://en.wikipedia.org/wiki/Resistor)
[[Apr 1st, 2023]]

- # References
	- https://grantwinney.com/using-pullup-and-pulldown-resistors-on-the-raspberry-pi/
	- https://www.electronics-tutorials.ws/logic/pull-up-resistor.html
	- https://learn.sparkfun.com/tutorials/pull-up-resistors/all)
- # Description
	- #+BEGIN_NOTE
	  Sa place dans le circuit détermine son nom
	  #+END_NOTE
	- Permet d'éviter d'avoir une valeur flottante / indéfinie lorsque le circuit est ouvert
	-
	- ## Résistance de rappel / *Pull-down resistor*
	  id:: 64287bf5-3871-41ed-9b00-98de29bb04b4
		- Se place **entre la ligne et la terre** pour permettre de garantir un état stable (qui ne dépend pas de l'environnement)
			- Lorsque le composant transmet un signal HIGH
				- La ligne est HIGH quand le circuit est fermée
					- Alimentation et terre connecté
				- La ligne est LOW quand le circuit est ouvert (déconnecté)
					- Connection vers la terre uniquement
	- ## Résistance de tirage / *Pull up resistor*
	  id:: 64287c00-cf70-4201-b24f-a0efe78451bb
		- Se place **entre la ligne et la source d'alimentation**  pour permettre de garantir un état stable (qui ne dépend pas de l'environnement)
			- Lorsque le composant transmet un signal LOW
				- La ligne est LOW quand le circuit est fermée (connectée à la terre)
				- La ligne est HIGH quand le circuit est ouvert