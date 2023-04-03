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
		- Valeur qui bascule de HIGH à LOW car la vraie valeur est intermédiaire due aux variations de l'environnement
	- ## Résistance de rappel / *Pull-down resistor*
	  id:: 64287bf5-3871-41ed-9b00-98de29bb04b4
		- Se place **entre la ligne et la terre** garantissant que :
			- La ligne est LOW quand le circuit est ouvert
				- Ligne **tirée** au niveau de la terre
			- La ligne est HIGH quand le circuit est fermée
				- Ligne au niveau de l'alimentation
	- ## Résistance de tirage / *Pull up resistor*
	  id:: 64287c00-cf70-4201-b24f-a0efe78451bb
		- Se place **entre la ligne et la source d'alimentation**  garantissant que :
			- La ligne est HIGH quand le circuit est ouvert
				- Ligne **tirée** au niveau de l'alimentation
			- La ligne est LOW quand le circuit est fermée
				- Ligne au niveau de la terre