alias:: Trackballs
[[Mar 26th, 2023]]

-
- # Roulements
	- ## Critères
	  id:: 6420511b-671b-4eea-955e-5e2e19d888a3
		- ### Régularité / Consistence (*Smoothness* / *Consistency*)
		  id:: 31530bd4-2d8e-4e65-bcaf-27676fd42145
			- Caractérise la continuité de la résistance pour toutes directions et vitesses
			- Une forte régularité donne un mouvement consistant sans irrégularité
				- Pas de sauts dans le suivi
				- Pas de sensation de sable coincé
				- Mouvement prédictible
		- ### Adhérence (*static friction* / *Stiction*)
		  id:: 2aabf780-9e90-4083-a893-bc08cb62555c
			- [Wikipédia](https://en.wikipedia.org/wiki/Stiction)
			- Caractérise la résistance à la mise en mouvement
				- Impacte la capacité à positionner précisément le curseur
				- Impacte la capacité à faire des petits déplacements
			- Une adhérence importante demande plus de force pour commencer à faire bouger la boule
		- ### Résistance aux frottements lors de la rotation (*rolling friction*)
		  id:: 5d2cd14b-8933-4114-a2bf-f3214ce9f9f1
			- [Wikipédia](https://en.wikipedia.org/wiki/Rolling)
			- Résistance au mouvement lorsque la balle est déjà en rotation
				- Impacte la capacité à faire naviguer rapidement le curseur sur de longues distances
				- Impacte la fluidité du mouvement sur
			- Une résistance importante entraîne une mise à l'arrêt rapide du mouvement de la boule
		- ### Bruit
		  id:: 6420512e-97f0-497b-a232-b2690e3f9813
			- Caractérise le niveau sonore lors du mouvement de la boule sur les roulements
	- ## Types
		- ### Billes en céramiques (*Static céramique bearings*)
		  id:: 4d11a85a-63b7-437d-b681-b8b1550b686a
			- ![Static_bearings](https://github.com/Wimads/Trackball-mousekeys-add-on-for-Skeletyl/raw/main/Images/Trackball%20static%20bearings.jpg){:height 250, :width 320}
			- Utilise des billes en céramiques ([Zro2 (zirconia) versus Si3N4 (silicon nitride)](https://prokcssmedia.blob.core.windows.net/sys-master-images/hb2/haf/9263251816478/ceramic-bearing-selection-guide.pdf))
				- La boule est en contact avec les trois billes qui sont elles statiques
				- Résistance aux frottements faible
					- La boule glisse sur les billes
				- Mécanisme très simple --> coût très faible
		- ### Roulements à rouleaux (*Roller bearings*)
			- ![Roller_bearings](https://github.com/Wimads/Trackball-mousekeys-add-on-for-Skeletyl/raw/main/Images/Roller%20bearings.jpg){:height 250, :width 320}
			- Axe de liberté unique
				- La résistance est dépendante de l'alignement entre l'axe du roulement et la direction de rotation de la boule
				- Peut entraîner des sauts / irrégularités suivant la direction de rotation de la boule
				- Mécanisme semi-complexe --> coût moyen
		- ### Unités de transfert à billes (*Ball transfer units / BTUs*)
			- ![BTUS_bearings](https://github.com/Wimads/Trackball-mousekeys-add-on-for-Skeletyl/raw/main/Images/Trackball%20BTU%20bearings.jpg){:height 250, :width 320}
			- Roulements omnidirectionnels sur une bille elle même en mouvement grâce à un ensemble de petites billes
				- Résistance au frottements réduits au minimum permettant de réduire le DPI du curseur
					- Amélioration de la précision sur de faibles mouvements
					- Mouvements importants toujours possibles grâce aux faibles frottements
				- Mécanisme complexe --> coût très important
	- ## Optimisation
	  id:: 642058ff-9b72-4fc5-9e06-f240063cb8df
		- La position des roulements par rapport à l'approche de la main joue un rôle important sur la réduction des frottements
		- La résistance (adhérance / frottements) est proportionelle à la masse et à la rugosité de la surface
		  id:: 287ec9cc-6a5a-464d-9390-6caf2441feb5
			- Prendre une boule plus légère
			- Polir la boule
			- Réduire la surface de contact entre les roulements et la boule