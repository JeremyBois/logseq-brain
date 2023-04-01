tags:: Hardware
alias:: Bascules, Flip-flop, Flip-flops
link:: [Wikipédia](https://en.wikipedia.org/wiki/Flip-flop_(electronics)) 
[[Apr 1st, 2023]]

- # Types
	- ## Set ($S$) Reset ($R$)
		- La sortie est noté $Q$ et son complément $\bar{Q}$ est l'opposé
			- $Q = 1 \rightarrow \bar{Q} = 0$
			- $Q = 0 \rightarrow \bar{Q} = 1$
		- **Active HIGH**
		  id:: 64286e05-25a6-4849-8cdc-d3d9c1a6b810
			- Utilise des portes logiques ((64286e6c-6645-4385-bea6-37e31aff7d75))
			- $S$ et $R$ doivent êtres maintenus à 0 (LOW)
			- Impulsion HIGH sur $S$ ou $R$ pour changer d'état
			- Nécessite une ((64287bf5-3871-41ed-9b00-98de29bb04b4))
		- **Active LOW**
			- Utilise des portes logiques ((64286e76-59c1-4722-8f80-69dc7b569f13))
			- $S$ (noté $\bar{S}$) et $R$ (noté $\bar{R}$) doivent êtres maintenus à 1 (HIGH)
			- Impulsion LOW sur $S$ ou $R$ pour changer d'état
			- Nécessite une ((64287c00-cf70-4201-b24f-a0efe78451bb))
		- #+BEGIN_IMPORTANT
		  Rebasculer $S$ et $R$ à la valeur courante en même temps donne un comportement indéterminé
		  #+END_IMPORTANT
		-