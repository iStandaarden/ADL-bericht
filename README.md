# ADL-bericht
XSD tbv ADL indicatie doorgave.

## Achtergrond
Vanaf 1 januari 2022 zal Functie ADL niet meer worden doorgegeven in de iWlz. Dit betekend dat de indicatie ADL (door het CIZ) direct aan de zorgaanbieders die ADL leveren moet worden doorgegeven. 
In de iWlz berichtketen zat hier het zorgkantoor nog tussen die een vertaling van het indicatiebericht (IO31) naar een toewijzingsbericht (AW33) maakte om die vervolgens aan de zorgaanbieder te sturen. 

## Nieuwe ADL xsd-bericht
Vanwege de huidige situatie waarin de zorgaanbieder een AW33 ontvangt is er voor gekozen om het nieuwe bericht zo veel mogelijk de iWlz iStandaard te laten volgen. Doordat het zorgkantoor geen rol meer heeft en omdat het CIZ geen AW33 aanleverd maar een IO31 is dat bericht als basis genomen met als argument:
* IO31.xsd is een iStandaard bericht wat het CIZ ook moet gebruiken binnen de iWlz-keten
* IO31.xsd en AW33.xsd hebben een gedeelde definitie waardoor betekenis van codelijsten gelijk is en is de structuur van de IO31 opgenomen in de AW33. Voor de softwareleverancier is het daardoor relatief eenvoudig het nieuwe bericht te implementeren. 

De definitie van het nieuwe bericht is [hier](/xsd) te vinden. 

De beschrijving en toelichting van de bericht elementen vind u [hier](ADL-berichtelement-beschrijving.md). 

laatste verie: ![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/tag/iStandaarden/ADL-bericht?style=flat-square)
