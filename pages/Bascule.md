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
			- Utilise des portes logiques ((64286e6c-6645-4385-bea6-37e31aff7d75))
			- $S$ et $R$ doivent êtres maintenus à 0 (LOW)
			- Impulsion HIGH sur $S$ ou $R$ pour changer d'état
			- Nécessite une [[Résistance]]
		- **Active LOW**
			- Utilise des portes logiques ((64286e76-59c1-4722-8f80-69dc7b569f13))
			- $S$ (noté $\bar{S}$) et $R$ (noté $\bar{R}$) doivent êtres maintenus à 1 (HIGH)
			- Impulsion LOW sur $S$ ou $R$ pour changer d'état
		- #+BEGIN_IMPORTANT
		  Rebasculer $S$ et $R$ à la valeur courante en même temps donne un comportement indéterminé
		  #+END_IMPORTANT
		-