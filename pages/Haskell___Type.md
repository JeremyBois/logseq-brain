tags:: Haskell
[[Jul 26th, 2023]]
***

- Construction de nouveau types
	- `newtype`
		- Construction d'un alias de type par encapsulation
			- Même représentation en mémoire au *runtime* que le type encapsulé
			- Pas d'impact sur les performances
		- Supporte un seul constructeur et un seul champ
		- ```haskell
		  newtype Vec2D = Vec2D  { unVec :: (Float, Float) }
		  
		  newtype Vec2D = Vec2D(Float, Float)
		  ```
	- `data`
		- Construction d'un nouveau type
			- Représentation en mémoire unique
		- Supporte plusieurs constructeurs et plusieurs champs
		- ```haskell
		  data Profession = Fighter | Archer | Accountant
		  data Race = Human | Elf | Orc | Goblin
		  
		  data Character = Character Race Profession
		  ```
		-
		-