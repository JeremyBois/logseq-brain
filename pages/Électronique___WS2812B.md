tags:: LED, PCB
alias:: Neopixel
***

- # Description
	- [[WS2812B datasheet]]
- # Utilisation
	- Nécessite une tension de 5V
		- Avec un [[RP2040]] il faut utiliser
		- Un réhausseur de tension (*level shifter*)
		- [SN74HCT08](https://www.ti.com/product/SN74HCT08) (8 bit)
		- [TXB0101](https://www.ti.com/product/TXB0101) (1 bit)
		- [74HCT245](https://www.nexperia.com/products/analog-logic-ics/logic/buffers-inverters-transceivers/transceivers/series/74HC245-74HCT245.html)
		- Utiliser uniquement du 3.3V pour les données et l'alimentation est aussi possible avec des limitations
			- Sensible aux perturbations, antennes, parasites, ...
			- La distance entre l'alimentation et la première #LED doit être la plus faible possible
			- La luminosité maximale est moins importante
			-
			-