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
- # Facteurs d'évaluations utilisés
	- Régularité (*smoothness*)
	  id:: 641ffa6e-f162-4fbd-a1f2-13f7cbec1446
		- Caractérise la continuité de la résistance pour toutes directions et vitesses
		- Une forte régularité donne un mouvement consistant sans irrégularité
			- Pas de sauts dans le suivi
			- Pas de sensation de sable coincé
	- Résistance à la mise en mouvement (*static friction*)
	  id:: 641ffab4-0d51-45cb-8610-d3d6fa2f93ff
		- Caractérise la résistance sur des micros mouvements
			- Impacte la capacité à positionner précisément le curseur
		- Une résistance importante demande plus de force pour commencer à faire bouger la boule
	- Résistance aux frottements (*rolling friction*)
	  id:: 641ffb4b-e14b-4040-8119-663e99f67c73
		- Résistance au mouvement lorsque la balle est déjà en rotation
			- Impacte la capacité à faire naviguer rapidement le curseur sur de longues distances
		- Une résistance importante entraîne une mise à l'arrêt rapide du mouvement de la boule
- ## Réduire la résistance aux frottements
	- La résistance est proportionelle à la masse et à la rugosité de la surface
		- Prendre une boule plus légère
		- Polir la boule
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
		- ((641ffa6e-f162-4fbd-a1f2-13f7cbec1446))
			- Bien
		- ((641ffab4-0d51-45cb-8610-d3d6fa2f93ff))
			- Normal
		- ((641ffb4b-e14b-4040-8119-663e99f67c73))
			- Normal
- ## Bille en céramiques (*Static céramique bearings*)
	- Utilise des billes en céramiques ([Zro2 (zirconia) versus Si3N4 (silicon nitride)](https://prokcssmedia.blob.core.windows.net/sys-master-images/hb2/haf/9263251816478/ceramic-bearing-selection-guide.pdf))
		- La boule est en contact avec les trois billes qui sont elles statiques
		- Résistance aux frottements faible
		- Mécanisme très simple --> coût très faible
	- Adaptateurs pour le modèle [[Ploopy/Classic]]
		- [Thingiverse](https://www.thingiverse.com/thing:4650448)
	- **Évaluation**
		- ((641ffa6e-f162-4fbd-a1f2-13f7cbec1446))
			- Excellent
		- ((641ffab4-0d51-45cb-8610-d3d6fa2f93ff))
			- Mauvais (même avec une boule plus légère)
		- ((641ffb4b-e14b-4040-8119-663e99f67c73))
			- Normal (même avec une boule plus légère)
- ## Unités de transfert à billes (*Ball transfer units*)
  id:: 78878d11-65fc-475e-b5be-cfa454f309cd
	- Roulements omnidirectionnels sur une bille elle même en mouvement grâce à un ensemble de petites billes
		- Résistance au frottements réduits au minimum
		- Mécanisme complexe --> coût très important
		-
		-
	- Positionnement
		- ![BTU_bearings_agencement.png](../assets/BTU_bearings_agencement_1679774067146_0.png){:height 200, :width 304}
		- Vertical
			- Base --> 60°
		- Inclinaison légère des BTUs