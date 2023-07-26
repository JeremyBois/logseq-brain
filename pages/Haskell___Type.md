tags:: Haskell
[[Jul 26th, 2023]]
***

- Construction de nouveau types
	- `newtype`
		- Construction d'un
		- Même représentation en mémoire au *runtime* que le type encapsulé
			- Un seul type peut être encapsulé
			- Pas d'impact sur les performances
	- `data`
		- Construction d'un nouveau type
			- Représentation en mémoire unique
		-