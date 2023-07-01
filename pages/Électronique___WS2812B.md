tags:: LED, PCB
alias:: Neopixel
***

- # Description
	- [[WS2812B datasheet]]
- # Utilisation
	- Nécessite une tension de 5V
		- Avec un [[RP2040]] il faut utiliser un réhausseur de tension (*level shifter*) comme un [SN74HCT08](https://www.ti.com/product/SN74HCT08)
		- Utiliser uniquement du 3.3V pour les données et l'alimentation est aussi possible avec des limitations
			- Sensible aux perturbations, antennes, parasites, ...
			- La distance entre l'alimentation et la première #LED doit être la plus faible possible
			- La luminosité maximale est moins importante
			-
			-