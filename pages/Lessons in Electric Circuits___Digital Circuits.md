type:: [[Book]]
author:: #[[Tony R. Kuphaldt]]
tags:: Électronique, Formation
link:: [PDF (original)](https://www.ibiblio.org/kuphaldt/electricCircuits/Digital/index.html)  [Online (All about circuit)](https://www.allaboutcircuits.com/textbook/digital/#chpt-3) 
[[Jul 2nd, 2023]]
***

- # Portes logiques (Logic Gates)
  id:: 64a1768f-99be-42da-a18c-c9ec66e2cdb3
	- ## Logic Signal Voltage Levels
		- type:: [[Article]]
		  link:: https://www.allaboutcircuits.com/textbook/digital/chpt-3/logic-signal-voltage-levels/
		- Un circuit de portes logiques acceptent en entrées comme en sorties uniquement deux types de signaux
		- Haut (1, *HIGH*) lorsque la tension d'alimentation est maximale
		- Bas (*0, LOW*) lorsque la tension d'alimentation est $0V$
		- ### Porte TTL
		  id:: 64a178e4-c096-4bd5-b3ef-f2f8b28aa424
			- Fonctionne uniquement pour une tension de $5.0V \pm 0.25V$
			- En pratique on a une marge de tolérance en entrée comme en sortie
				- ![voltage tolerance of ttl gate inputs](https://www.allaboutcircuits.com/uploads/articles/voltage-tolerance-of-ttl-gate-inputs.jpg){:height 236, :width 478}
				- Sortie **non utilisable** directement en entrée d'une ((64a17b2c-4eae-40e5-84c7-54de6459807a))
					- Une ((64287c00-cf70-4201-b24f-a0efe78451bb)) est nécessaire pour garantir que le signal HIGH sera correctement interprété
						- Doit être mise sur l'alimentation
			- La marge de bruit entre deux portes TTL est calculée en fonction de la différence de la marge entre l'entrée et la sortie
			  id:: 64a17a08-c0fe-4567-bc29-9a1607b34789
				- *LOW* --> 0.3V
				- *HIGH* --> 0.7V
				- Supporte moins de variations parasitaires qu'une porte **CMOS**
				- Utilisable pour réhausser un signal si on veut communiquer avec un système fonctionnant en $5V$ depuis un MCU fonctionnant en $3.3V$
			- ### Porte CMOS
			  id:: 64a17b2c-4eae-40e5-84c7-54de6459807a
				- Supporte une large palette de tensions pour les signaux ($0 \to 15V$)
				- En pratique on a une marge de tolérance en entrée comme en sortie
				- ![voltage tolerance of cmos gate inputs](https://www.allaboutcircuits.com/uploads/articles/voltage-tolerance-of-cmos-gate-inputs.jpg){:height 220, :width 494}
					- Sortie **utilisable** en entrée d'une ((64a178e4-c096-4bd5-b3ef-f2f8b28aa424))
				- La marge de bruit entre deux portes TTL est calculée en fonction de la différence de la marge entre l'entrée et la sortie
					- *LOW* --> 1.45V
					- *HIGH* --> 1.45V
					- Support plus de variations parasitaires qu'une porte **TTL**
					- Ne permet pas de coupler logique $3.3V$ et logique $5.0V$
			-
				-