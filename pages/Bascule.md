tags:: Hardware
alias:: Bascules, Flip-flop, Flip-flops
link:: [Wikipédia](https://en.wikipedia.org/wiki/Flip-flop_(electronics)) 
[[Apr 1st, 2023]]

- # Types
	- ## Set ($S$) Reset ($R$)
		- La sortie est noté $Q$ et sont complément $\bar{Q}$ est l'opposé
			- $Q = 1 \rightarrow \bar{Q} = 0$
			- $Q = 0 \rightarrow \bar{Q} = 1$
		- **Active high**
			- Utilise des [[Porte Logique]] *NOR*
			- $S$ et $R$ sont la plupart du temps à 0
			- On change temporairement (impulsion) $S$ ou $R$ à 1 pour changer d'état
			-
		- **Active low**
			- Utilise des portes logiques NAND
			- $S$ (noté $\bar{S}$) et $R$ (noté $\bar{R}$) sont la plupart du temps à 1
			- On change temporairement (impulsion) $S$ ou $R$ à 0 pour changer d'état
		- #+BEGIN_IMPORTANT
		  Rebasculer $S$ et $R$ à la valeur courante en même temps est indéterminé et ne doit jamais arriver
		  #+END_IMPORTANT
-