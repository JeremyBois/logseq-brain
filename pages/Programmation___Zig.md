tags:: Embarqué, Backend, CLI
alias:: Zig, Ziglang, Zig Lang
link:: [Official](https://ziglang.org/) [Github](https://github.com/ziglang/zig) 
[[Aug 27th, 2023]]
***

- ↳ [[Programmation]] 
  {{namespace Zig}}
  ***
- ![Zig logo](https://miro.medium.com/fit/c/224/224/1*b3og8n0fDkAnHUx-0lDMHg.png)
- **Le successeur du [[Programming/C]]** combinant vitesse et simplicité**
- # Ressources
	- Référence / Documentation
		- [ziglang.org](https://ziglang.org/documentation/master/)
	- Forum
		- [ziggit.dev](https://ziggit.dev/)
	- Infos / Articles
		- [zig.news](https://zig.news/)
- # Points forts
	- Compilation
		- Rapide
		- Multi-platformes
		- Intégré au langage
			- Utilise **Comptime**
		- Compatible avec [[Programmation/C]]
			- Transpilation du code + encapsulation dans la sortie
			- Transpilation des macros
		- Peut compiler du C/C++
			- Potentiel de remplacer [[Programmation/Cmake]], [[Programmation/Premake]], ...
		- Pas de macros / préprocesseurs
			- Utilise **Comptime**
	- Utilisation
		- Paradigme non Orienté Objet
		- Simple et pragmatique
		- Pointeurs non null ou optionnels
		- Erreurs en retour de fonction
		- Pas de bouclage auto pour les `uint` par défaut
			- Possible de le demander explicitement
		- Test intégrés
- # Domaines
	- Embarqué
		- [Microzig](https://github.com/ZigEmbeddedGroup/microzig)
			- Support pour #RP2040
	- Jeu vidéo
		- [Zig-Gamedev](https://github.com/michal-z/zig-gamedev)
			- Boîte à outils / Ensemble de bibliothèques
-