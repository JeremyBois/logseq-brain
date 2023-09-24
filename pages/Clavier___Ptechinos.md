tags:: PCB, CAD, Projet, Clavier
author:: #[[Jérémy Bois]]
alias:: Ptechinos
link:: [PCB](https://github.com/JeremyBois/Ptechinos) [Layout](https://github.com/JeremyBois/qmk-ptechinos)
[[Feb 23rd, 2023]]
***

- ↳ [[Clavier]]
  {{namespace Ptechinos}}
  ***
- # Tâches
	- DONE Prévoir plus de marge verticalement pour les switches au niveau des encodeurs
		- Il doit être possible de retirer la *top plate* avec les switches soudés
	- DONE Refaire le PCB pour le capteur #Kicad
		- [Ogen](https://github.com/JeremyBois/Ogen) n'a pas de distinction de voltage sur les différents VDD alors qu'il faudrait du 3.3V et du 1.9V pour être cohérent
		- Régulateurs de courant
			- Sortie ajustable
				- [AP2127K-ADJTRG1](https://www.lcsc.com/product-detail/Linear-Voltage-Regulators-LDO_Diodes-Incorporated-AP2127K-ADJTRG1_C96343.html)
					- Nécessite 2 résistances pour fixer la tension de sortie
			- Sortie fixe :
				- --> 1.9V [VRH1902LTX](https://www.lcsc.com/product-detail/Linear-Voltage-Regulators-LDO_AnaSem-VRH1902LTX_C697975.html)
				- --> 3.3V [AP2127K-3-3TRG1](https://www.lcsc.com/product-detail/Linear-Voltage-Regulators-LDO_Diodes-Incorporated-AP2127K-3-3TRG1_C156285.html)
	- DONE Solutions pour un soucis de tracking #Trackball #QMK
		- Vérifier la distance capteur/balle
		- Modifier `PMW33XX_LIFTOFF_DISTANCE`
		- [Reddit](https://www.reddit.com/r/ErgoMechKeyboards/comments/12x70nm/any_instructions_how_to_configure_trackball_via/)
	- DONE Soucis lors l'envoi de certaines touches
		- `e`  et `espace` sortent en double assez souvent
		- Observé sur Windows avec la version **0.6** avec #Promicro
		- Non observée sur la version v0.69 avec #RP2040
	- DONE Implémenter le code pour le support des périphérique de pointage
	- DONE Souder le pont JP1 pour ajouter la ((64287c00-cf70-4201-b24f-a0efe78451bb)) sur la ligne MISO #Trackball
		- [Github Ogen PCB](https://github.com/JeremyBois/Ogen)
		- [MISO peut être flottant car contrôlée par l'esclave uniquement](https://electronics.stackexchange.com/a/234707)
	- DONE Adoucir le son du Clavier #Foam
	  id:: 64da80fd-a516-476c-b4a9-8cb1c58996eb
		- Matériaux
			- Éthylène-acétate de vinyle (EVA)
				- Très bonne atténuation
				- anti statique
			- Uréthane (Poron)
				- Bonne atténuation
				- anti statique
			- Polyéthylène (PE)
				- Réflection du son
					- Donne un effet unique au son
					- Évite la propagation vers le bas du boitier
				- **Peut entraîner des #ESD** si il n'est pas spécialement développé pour avoir des propriétés anti-statiques
			- Tissu de liège
				- Actuellement du 0.5mm de disponible
			- Cuir
				- Naturel
				- **Odorant**
			- Liège
				- Naturel