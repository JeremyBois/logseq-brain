alias:: Csharp

-
- # Ressources
	- Parameter passing in C#
	  id:: 642ec8af-2ddf-4bf9-92ce-6b32af763694
	  type:: [[Article]]
	  author:: #[[Jon Skeet]]
	  link:: https://jonskeet.uk/csharp/parameters.html
		- Intéressant pour bien comprendre comment et quand utiliser `ref` / `out` sur des `class`  ou des `struct`
	- Tutorial: Reduce memory allocations with `ref` safety
	  id:: 644a71f1-1842-44d5-a848-11282a455dcc
	  type:: [[Article]]
	  author:: #Microsoft
	  link:: https://learn.microsoft.com/en-us/dotnet/csharp/advanced-topics/performance/ref-tutorial
		- Optimiser la mémoire
			- Allouer les données sur la [[Programmation/Pile]] en utilisant des `struct`
			- Limiter les copies en utilisant des références vers ces `struct`
		- Documenter le code avec la sémantique du langage
			- Référence en lecture seule --> `in`
				- ```cs
				  public void AddMeasurement(in SensorMeasurement datum)
				  ```
			- Référence modifiable
				- Variable déjà initialisée --> `ref`
				- Variable pas forcément initialisé --> `out`
			- Référence de retour en lecture seule `ref readonly `
				- ```cs
				  public  ref readonly AverageMeasurement Average { get { return ref average; } }
				  ```
			-