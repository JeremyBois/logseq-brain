alias:: Trackballs
[[Mar 26th, 2023]]

-
- # Roulements
	- ## Critères
	  id:: 6420511b-671b-4eea-955e-5e2e19d888a3
		- ### Régularité / Consistence (*Smoothness* / *Consistency*)
		  id:: 31530bd4-2d8e-4e65-bcaf-27676fd42145
		  collapsed:: true
			- Caractérise la continuité de la résistance pour toutes directions et vitesses
			- Une forte régularité donne un mouvement consistant sans irrégularité
			  collapsed:: true
				- Pas de sauts dans le suivi
				- Pas de sensation de sable coincé
				- Mouvement prédictible
		- ### Adhérence (*static friction* / *Stiction*)
		  id:: 2aabf780-9e90-4083-a893-bc08cb62555c
		  collapsed:: true
			- [Wikipédia](https://en.wikipedia.org/wiki/Stiction)
			- Caractérise la résistance à la mise en mouvement
			  collapsed:: true
				- Impacte la capacité à positionner précisément le curseur
				- Impacte la capacité à faire des petits déplacements
			- Une adhérence importante demande plus de force pour commencer à faire bouger la boule
		- ### Résistance aux frottements lors de la rotation (*rolling friction*)
		  id:: 5d2cd14b-8933-4114-a2bf-f3214ce9f9f1
		  collapsed:: true
			- [Wikipédia](https://en.wikipedia.org/wiki/Rolling)
			- Résistance au mouvement lorsque la balle est déjà en rotation
			  collapsed:: true
				- Impacte la capacité à faire naviguer rapidement le curseur sur de longues distances
				- Impacte la fluidité du mouvement sur
			- Une résistance importante entraîne une mise à l'arrêt rapide du mouvement de la boule
		- ### Bruit
		  collapsed:: true
			- Caractérise le niveau sonore lors du mouvement de la boule sur les roulements
	- ## Optimiser les critères
		- La résistance (adhérance / frottements) est proportionelle à la masse et à la rugosité de la surface
		  collapsed:: true
			- Prendre une boule plus légère
			- Polir la boule
			- Réduire la surface de contact entre les roulements et la boule
	- ## Types
	  id:: 64205b96-5560-47cd-861d-1885c58902a1
		- ### Roulements à rouleaux (*Roller bearings*)
		  id:: 64205bce-7423-4e78-a095-efffe3ac9caa
			- ![]
			- Axe de liberté unique
				- La résistance est dépendante de l'alignement entre l'axe du roulement et la direction de rotation de la boule
				- Peut entraîner des sauts / irrégularités suivant la direction de rotation de la boule
				- Mécanisme semi-complexe --> coût moyen
		- ### Bille en céramiques (*Static céramique bearings*)
		  collapsed:: true
			- Utilise des billes en céramiques ([Zro2 (zirconia) versus Si3N4 (silicon nitride)](https://prokcssmedia.blob.core.windows.net/sys-master-images/hb2/haf/9263251816478/ceramic-bearing-selection-guide.pdf))
				- La boule est en contact avec les trois billes qui sont elles statiques
				- Résistance aux frottements faible
				- Mécanisme très simple --> coût très faible
		- ### Unités de transfert à billes (*Ball transfer units / BTUs*)
			- Roulements omnidirectionnels sur une bille elle même en mouvement grâce à un ensemble de petites billes
				- Résistance au frottements réduits au minimum permettant de réduire le DPI du curseur
					- Amélioration de la précision sur de faibles mouvements
					- Mouvements importants toujours possibles grâce aux faibles frottements
				- Mécanisme complexe --> coût très important
		-