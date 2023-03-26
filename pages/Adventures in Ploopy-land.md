type:: [[Article]]
author:: #[[George Bryant]]
tags:: Ploopy, Trackball
link:: [Blog](https://www.gbryant.co.uk/posts/2021-02-15_ploopy-trackball/post.html)
[[Mar 25th, 2023]]

- ***
	- Études des différents types de bearings pour améliorer la trackball [[Ploopy/Classic]]
		- Original --> ((762fa0d6-cb08-482f-8b41-26bebf932d17))
		- Mod --> ((78878d11-65fc-475e-b5be-cfa454f309cd))
- ***
- # Types de bearings
- ## Roulements à rouleaux (*Roller bearings*)
  id:: 762fa0d6-cb08-482f-8b41-26bebf932d17
	- Utilise des roulements avec un unique axe de liberté sur lequel il tourne
		- La résistance est dépendante de l'alignement entre l'axe du roulement et la direction de rotation de la boule
		- Peut entraîner des sauts / irrégularités suivant la direction de rotation de la boule
		- Mécanisme semi-complexe --> coût moyen
	- Positionnement
		- ![Roller_bearings_agencement.png](../assets/Roller_bearings_agencement_1679773909456_0.png){:height 180, :width 304}
		- Vertical
			- Base --> 60°
			- Surhaussement de celui au niveau du poignet pour améliorer la stabilité --> 77°
	- **Évaluation**
		- ((31530bd4-2d8e-4e65-bcaf-27676fd42145))
			- Bien
		- ((2aabf780-9e90-4083-a893-bc08cb62555c))
			- Normal
		- ((5d2cd14b-8933-4114-a2bf-f3214ce9f9f1))
			- Normal
- ## Bille en céramiques (*Static céramique bearings*)
	- Utilise des billes en céramiques ([Zro2 (zirconia) versus Si3N4 (silicon nitride)](https://prokcssmedia.blob.core.windows.net/sys-master-images/hb2/haf/9263251816478/ceramic-bearing-selection-guide.pdf))
		- La boule est en contact avec les trois billes qui sont elles statiques
		- Résistance aux frottements faible
		- Mécanisme très simple --> coût très faible
	- ![Support avec billes en céramiques](https://www.gbryant.co.uk/posts/2021-02-15_ploopy-trackball/img/2021-02-08_0001.jpg){:height 216, :width 330}
	- Adaptateurs pour le modèle [[Ploopy/Classic]]
		- [Thingiverse](https://www.thingiverse.com/thing:4650448)
	- **Évaluation**
		- ((31530bd4-2d8e-4e65-bcaf-27676fd42145))
			- Excellent
		- ((2aabf780-9e90-4083-a893-bc08cb62555c))
			- Mauvais (même avec une boule plus légère)
		- ((5d2cd14b-8933-4114-a2bf-f3214ce9f9f1))
			- Normal (même avec une boule plus légère)
- ## Unités de transfert à billes (*Ball transfer units / BTUs*)
  id:: 78878d11-65fc-475e-b5be-cfa454f309cd
	- Roulements omnidirectionnels sur une bille elle même en mouvement grâce à un ensemble de petites billes
		- Résistance au frottements réduits au minimum permettant de réduire le DPI du curseur
			- Amélioration de la précision sur de faibles mouvements
			- Mouvements importants toujours possibles grâce aux faibles frottements
		- Mécanisme complexe --> coût très important
	- Adaptateurs pour le modèle [[Ploopy/Classic]] avec 8mm BTU Bosch-Rexroth R053010810 (ou KU-B8-OFK)
		- [Github](https://github.com/ploopyco/classic-trackball/tree/master/hardware/Mechanicals-BTU-Mod)
	- ![Support avec BTUs](https://www.gbryant.co.uk/posts/2021-02-15_ploopy-trackball/img/2021-02-08_0006.jpg){:height 216, :width 330}
	- Positionnement
		- ![BTU_bearings_agencement.png](../assets/BTU_bearings_agencement_1679774067146_0.png){:height 200, :width 304}
		- Vertical
			- Base --> 60°
		- Inclinaison légère des BTUs
	- **Évaluation**
		- ((31530bd4-2d8e-4e65-bcaf-27676fd42145))
			- Bien
			- Peu prendre un peu de temps pour se stabiliser
			- Irrégularités principalement sur les mouvements importants
		- ((2aabf780-9e90-4083-a893-bc08cb62555c))
			- Excellent
		- ((5d2cd14b-8933-4114-a2bf-f3214ce9f9f1))
			- Excellent