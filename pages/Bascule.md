tags:: Hardware
alias:: Bascules, Latch, Latches
link:: [Wikipédia](https://en.wikipedia.org/wiki/Flip-flop_(electronics)) 
[[Apr 1st, 2023]]

- # Description
	- La sortie est noté $Q$ et son complément $\bar{Q}$ est l'opposé
		- $Q = 1 \rightarrow \bar{Q} = 0$
		- $Q = 0 \rightarrow \bar{Q} = 1$
- # Fonctionnement
	- **Active HIGH**
		- État normal LOW (0)
		- Impulsion HIGH (1) pour changer d'état
		- Nécessite une ((64287bf5-3871-41ed-9b00-98de29bb04b4))
	- **Active LOW**
		- État normal HIGH (1)
		- Impulsion LOW (0) pour changer d'état
		- Nécessite une ((64287c00-cf70-4201-b24f-a0efe78451bb))
	- ## Set ($S$) Reset ($R$)
		- **Active HIGH**
		  id:: 64286e05-25a6-4849-8cdc-d3d9c1a6b810
			- Utilise des portes logiques ((64286e6c-6645-4385-bea6-37e31aff7d75))
			- $S$ et $R$ doivent êtres maintenus à 0 (LOW)
			- Impulsion HIGH (1) sur $S$ ou $R$ pour changer d'état
			- ![SR_nor](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.stack.imgur.com%2Fog9PY.png&f=1&nofb=1&ipt=7095434b3d812c5c07841a08961538ec675ac3c034a5408abdd895e0ff330ffc&ipo=images)
		- **Active LOW**
			- ![Latch_SR_nand](https://upload.wikimedia.org/wikipedia/commons/thumb/9/92/SR_Flip-flop_Diagram.svg/330px-SR_Flip-flop_Diagram.svg.png)
			- Utilise des portes logiques ((64286e76-59c1-4722-8f80-69dc7b569f13))
			- $S$ (noté $\bar{S}$) et $R$ (noté $\bar{R}$) doivent êtres maintenus à 1 (HIGH)
			- Impulsion LOW sur $S$ ou $R$ pour changer d'état
		- #+BEGIN_IMPORTANT
		  Rebasculer $S$ et $R$ à la valeur courante en même temps donne un comportement indéterminé
		  #+END_IMPORTANT
	- ## Gated ($E$) Set ($S$) Reset ($R$)
		- Ajout des portes logiques ((64286e76-59c1-4722-8f80-69dc7b569f13))
		- ![Latch_gsr](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/SR_%28Clocked%29_Flip-flop_Diagram.svg/300px-SR_%28Clocked%29_Flip-flop_Diagram.svg.png)