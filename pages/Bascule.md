tags:: Hardware
alias:: Bascules, Flip-flop, Flip-flops
link:: [Wikipédia](https://en.wikipedia.org/wiki/Flip-flop_(electronics)) 
[[Apr 1st, 2023]]

- # Types
	- ## Set ($S$) Reset ($R$)
		- **Active high**
			- Utilise des portes logiques *NOR*
			- $S$ et $R$ sont la plupart du temps à 0
			- On bascule **temporairement** $S$ ou $R$ à 1 pour changer d'état
		- **Active low**
			- Utilise des portes logiques NAND
			- $S$ et $R$ sont la plupart défaut à 1
				- Souvent on utilise $\bar{S}$ et $\bar{R}$
			- On bascule **temporairement** $S$ ou $R$ à 0 pour changer d'état
		- Rebasculer à la valeur par défaut sur $S$ et $R$ en même temps est indéterminé et ne doit pas arriver
		- La sortie est noté $Q$ et sont complément $\bar{Q}$ et est
-