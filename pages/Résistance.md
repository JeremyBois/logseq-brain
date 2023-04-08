tags:: Harware, Software
alias:: Résistances, Resistor, Resistors 
link:: [Wikipédia](https://en.wikipedia.org/wiki/Resistor)
[[Apr 1st, 2023]]

- # References
	- https://grantwinney.com/using-pullup-and-pulldown-resistors-on-the-raspberry-pi/
	- https://www.electronics-tutorials.ws/logic/pull-up-resistor.html
	- https://learn.sparkfun.com/tutorials/pull-up-resistors/all)
- # Description
	- Permet d'éviter d'avoir une valeur **flottante** / indéfinie lorsque le circuit est ouvert
		- Valeur qui bascule de HIGH à LOW car la vraie valeur est intermédiaire due aux variations de l'environnement
	- Plus la résistance est importante moins de courant traverse
		- Résistance faible --> Plus de courant passe au travers
			- Pull-up / Pull-down forte
		- Résistance forte --> Moins de courant passe au travers
			- Pull-up / Pull-down faible
	- #+BEGIN_IMPORTANT
	  L'importance de la résistance est toujours relative au reste du circuit. 
	  #+END_IMPORTANT
	- ## Résistance de rappel / *Pull-down resistor*
	  id:: 64287bf5-3871-41ed-9b00-98de29bb04b4
		- Se place **entre la ligne et la terre** garantissant que :
			- La ligne est HIGH quand le circuit est fermée
				- Ligne au niveau de l'alimentation
			- La ligne est LOW quand le circuit est ouvert
				- Ligne **tirée** au niveau de la terre
		- Si un circuit connecte 3.3V à un GPIO
			- Ligne HIGH quand le circuit est fermée
			- Ligne LOW car tirée vers la terre quand il est ouvert
	- ## Résistance de tirage / *Pull up resistor*
	  id:: 64287c00-cf70-4201-b24f-a0efe78451bb
		- Se place **entre la ligne et la source d'alimentation**  garantissant que :
			- La ligne est LOW quand le circuit est fermée
				- Ligne au niveau de la terre
			- La ligne est HIGH quand le circuit est ouvert
				- Ligne **tirée** au niveau de l'alimentation
		- Si un circuit connecte la terre à un GPIO
			- Ligne LOW quand le circuit est fermée
			- Ligne HIGH car tirée vers 3.3V quand il est ouvert