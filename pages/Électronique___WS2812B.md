tags:: LED, PCB
alias:: Neopixel
***

- # Description
	- [[WS2812B datasheet]]
- # Utilisation
	- Nécessite une tension de 5V
		- Avec un [[RP2040]] il faut utiliser
		- Un réhausseur de tension (*level shifter*)
			- N'inversant pas la valeur logique in/out
			- Compatible avec des entrées TTL
			- Supportant une alimentation de 5V
			- [SN74HCT08](https://www.ti.com/product/SN74HCT08) (8 bit)
			- [TXB010x](https://www.ti.com/sitesearch/en-us/docs/universalsearch.tsp?langPref=en-US&searchTerm=TXB010&nr=3#q=TXB010&sort=relevancy&numberOfResults=25) (x bits)
			- [74HCT245](https://www.nexperia.com/products/analog-logic-ics/logic/buffers-inverters-transceivers/transceivers/series/74HC245-74HCT245.html)
			-
		- Utiliser uniquement du 3.3V pour les données et l'alimentation est aussi possible avec des limitations
			- Sensible aux perturbations, antennes, parasites, ...
			- La distance entre l'alimentation et la première #LED doit être la plus faible possible
			- La luminosité maximale est moins importante
			-
			-