tags:: Hardware
alias:: Bascules, Latch, Latches, Flip-Flop, Flip-Flops
link:: [Wikipédia](https://en.wikipedia.org/wiki/Flip-flop_(electronics)) [Youtube Playlist](https://www.youtube.com/watch?v=-aQH0ybMd3U&list=PLTd6ceoshpreKyY55hA4vpzAUv9hSut1H)
[[Apr 1st, 2023]]

- # Avancement
	- TODO D Type FlipFlop (5)
	- TODO JK Flip-Flop (6)
- # Principe
	- Utilisation
		- Stabilisation d'un changement de signal
		- Mémoriser un bit d'information
		- Bloc de base pour construire des [[Registre à décalage]]
	- **Active HIGH**
	  id:: 64289354-60ce-4bbb-a17e-7cfbe5e8894f
		- État normal LOW (0)
		- Impulsion HIGH (1) pour changer d'état
		- Nécessite une ((64287bf5-3871-41ed-9b00-98de29bb04b4))
	- **Active LOW**
	  id:: 6428918c-6d63-43ed-8ce0-6154ff6782ff
		- État normal HIGH (1)
		- Impulsion LOW (0) pour changer d'état
		- Nécessite une ((64287c00-cf70-4201-b24f-a0efe78451bb))
- # Nomenclature
	- La sortie est noté $Q$ et son complément $\bar{Q}$ est l'opposé
		- $Q = 1 \rightarrow \bar{Q} = 0$
		- $Q = 0 \rightarrow \bar{Q} = 1$
- # Set ($S$) Reset ($R$)
	- ![Latch_SR_nor_nand](https://image1.slideserve.com/2405882/sr-latch-l.jpg){:height 308, :width 387}
	- SR ((64286e6c-6645-4385-bea6-37e31aff7d75))
	  id:: 64286e05-25a6-4849-8cdc-d3d9c1a6b810
		- ((64289354-60ce-4bbb-a17e-7cfbe5e8894f))
		- $S$ et $R$ doivent êtres maintenus à LOW (0)
		- Impulsion HIGH (1) sur $S$ ou $R$ pour changer d'état
	- SR ((64286e76-59c1-4722-8f80-69dc7b569f13))
	  id:: 64286e05-6815-4a91-af29-b1c5c34ef6c6
		- ((6428918c-6d63-43ed-8ce0-6154ff6782ff))
		- $\bar{S}$ et $\bar{R}$ doivent êtres maintenus HIGH (1)
		- Impulsion LOW (0) sur $\bar{S}$ ou $\bar{R}$ pour changer d'état
	- Gated
		- ![Latch_gsr](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/SR_%28Clocked%29_Flip-flop_Diagram.svg/300px-SR_%28Clocked%29_Flip-flop_Diagram.svg.png)
		- ((64289354-60ce-4bbb-a17e-7cfbe5e8894f))
		- Ajout des portes logiques ((64286e76-59c1-4722-8f80-69dc7b569f13)) pour connecter la nouvelle ligne $E$
		- La ligne $E$ permet de contrôler la fenêtre durant laquelle la bascule est active
		- Un changement d'état n'a d'effets que si l'impulsion arrive alors que la ligne $E$ est HIGH
	- #+BEGIN_IMPORTANT
	  Rebasculer $S$ et $R$ à la valeur courante en même temps donne un comportement indéterminé
	  #+END_IMPORTANT
- # Data / Gated Data
	- | ((64286e05-6815-4a91-af29-b1c5c34ef6c6)) | ((64286e05-25a6-4849-8cdc-d3d9c1a6b810)) |
	  |:-:|:-:|
	  | ![Latch_d_nand](https://upload.wikimedia.org/wikipedia/commons/2/2f/D-Type_Transparent_Latch.svg){:height 159, :width 300} | ![Latch_d_nor](https://upload.wikimedia.org/wikipedia/commons/c/cb/D-type_Transparent_Latch_%28NOR%29.svg) |
	- Une seule ligne ($D$) pour contrôler la sortie $Q$
		- Sert à la fois de set et de reset
	- La ligne $E$ permet de contrôler la fenêtre durant laquelle la bascule est active
	- Persistence / mémoire de la variation de la ligne $D$
		- Impulsion HIGH sur $D$ et $E$ est HIGH
			- $Q$ est HIGH
		- Impulsion HIGH sur $D$ et $E$ est LOW
			- $Q$ HIGH **dès que** $E$ bascule en HIGH
- # Clocked Data
	- La ligne $E$ est contrôlé par une horloge et renommée $C$
		- Chaque impulsion arrive à une certaine fréquence
		- Permet de synchroniser la période d'activation de plusieurs bascules
	- Ajout de la détection d'un [front montant](https://fr.wikipedia.org/wiki/Flanc_(%C3%A9lectronique))
		- Utilisation de la latence entre les portes logiques pour la détection en combinant un nombre impair de portes logiques ((64286e0a-9764-4f9e-8a5b-6cb3509aa93f)) et une porte logique ((64286e1e-893f-45a3-860b-6027376bfb68))
		- ![Risingedge_detector](https://i.stack.imgur.com/GHbcC.png){:height 113, :width 367}
		- Évite que la synchronisation soit dépendante de la fréquence de l'horloge
		- Permet de synchroniser le moment de la mise à jour de $Q$ sur différentes bascules
	- Ajout de deux nouvelles lignes permettant un contrôle asynchrone de la sortie $Q$ indépendament de l'état de $D$ ou $C$
		- $PRE$ permet de forcer $Q$ à HIGH
		- $CLR$ permet de forcer $Q$ à LOW
	- Permet le stockage d'un bit de mémoire
		- Utilisation dans les [[Registre à décalage]] ou les compteurs