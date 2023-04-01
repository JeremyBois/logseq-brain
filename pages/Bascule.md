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
			- Utilise des portes logiques *NOR*
			- $S$ et $R$ sont la plupart du temps à 0
			- On change temporairement (impulsion) $S$ ou $R$ à 1 pour changer d'état
		- **Active low**
			- Utilise des portes logiques NAND
			- $S$  (aussi noté)et $R$ sont la plupart défaut à 1
				- Souvent on utilise $\bar{S}$ et $\bar{R}$ au lieu de $S$ et $R$ pour éviter la confusion avec une bascule active high
			- On change temporairement (impulsion) $S$ ou $R$ à 0 pour changer d'état
		- Rebasculer $S$ et $R$ à la valeur courante en même temps est indéterminé et ne doit pas arriver
-