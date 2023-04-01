tags:: Hardware
alias:: Bascules, Latch, Latches
link:: [Wikipédia](https://en.wikipedia.org/wiki/Flip-flop_(electronics)) 
[[Apr 1st, 2023]]

- # Principe
	- La sortie est noté $Q$ et son complément $\bar{Q}$ est l'opposé
		- $Q = 1 \rightarrow \bar{Q} = 0$
		- $Q = 0 \rightarrow \bar{Q} = 1$
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
- # Types
	- ## Set ($S$) Reset ($R$)
		- ![Latch_SR_nor_nand](https://image1.slideserve.com/2405882/sr-latch-l.jpg){:height 280, :width 450}
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
			- La ligne $E$ permet de limiter l'effet de bascule indépendament des changements sur $S$ et $R$
				- Permet un changement uniquement dans certaines conditions
		- #+BEGIN_IMPORTANT
		  Rebasculer $S$ et $R$ à la valeur courante en même temps donne un comportement indéterminé
		  #+END_IMPORTANT
	- ## Data $D$
		- | ((64286e05-6815-4a91-af29-b1c5c34ef6c6)) | ((64286e05-6815-4a91-af29-b1c5c34ef6c6)) |
		  |:-:|:-:|
		  | ![Latch_d](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/D-Type_Transparent_Latch.svg/676px-D-Type_Transparent_Latch.svg.png){:height 217, :width 279} | ![Latch_d](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/D-Type_Transparent_Latch.svg/676px-D-Type_Transparent_Latch.svg.png){:height 217, :width 279} |
		- Un unique