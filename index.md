# PORTFOLIO
*Bram Slemmer, 14081563*

## Leeswijzer
In dit portfolio staat wat ik heb gedaan in het afgelopen half jaar in de Data Science minor.
Hieronder staan uitgeschreven wat mijn bijdragen zijn geweest aan het project met daarnaast nog een link naar de verschillende opdrachten zoals coursera die we af moesten hebben.

[Opdrachten](https://bram4370.github.io/portfolioDataScience/Opdrachten/Opdrachten)

## Opstarten van het project

Bij het opstarten van het project heb ik onderzoek gedaan naar de technische domeinkennis over het tracken van mensen en het werken met de RealSense zr300 camera. In het vooronderzoek document heb ik een aantal links geplaats naar gevonden informatie.
- [Vooronderzoek.pdf](documents/Aanpak_vooronderzoek.pdf){:target="_blank"}

## Intel Realsense ZR300

Ik heb in het begin veel gewerkt met de Intel camera.

<img src=/images/Printscreen_camera.png width="600" he3ght="300">

*het eerste beeld wat ik kreeg was het beeld wat je hierboven ziet. Aan de rechterkant zie je het dieptebeeld wat wij kregen van het linkerbeeld*

De beelden hiervan moesten wij opslaan samen met de diepte die we terugkregen per punt. Dit werd gedaan door de dieptes die we terugkregen van de camera uitgedrukt in het aantal centimeter aan afstand van de camera uit te schrijven naar de terminal en die output weer op te slaan in een csv bestand. Het resultaat was een groot bestand met allemal cijfers zoals hieronder.

![CSV beelden camera](/images/combined_frames_csv.png)

Deze beelden konden wij dan weer omzetten door een grijswaarde te geven aan de cellen op basis van de waarde in de cellen. Daardoor kregen wij een soort van visuele representatie op van wat wij opslaan. Dit resultaat is hieronder weergeven

![Greyscale image realsense](/images/Frame1.png)

Het probleem wat wij hier hadden was dat de camera niet erg nauwkeurig leek te zijn. Er zaten zoals hierboven te zien is veel gaten in de beelden die wij opnamen. Ik heb zelf nog geprobeerd om dit op te lossen door een gemiddelde te nemen van een aantal frames wat wel een deel van de gaten liet verdwijnen of minder maakte maar de vraag was of dit wel genoeg was voor ons doel.

![Average greyscale image realsense](/images/Frame_average.png)

Daarnaast hebben wij zitten zoeken naar een manier om de joint van mensen te tracken op de beelden die wij opnemen. Helaas was de SDK die beschikbaar was al enige tijd niet meer verder ontwikkeld en heeft Intel de ontwikkelink hiervan compleet stop gezet. Daarnaast waren er ook verder geen duidelijke oplossingen om dit te doen.

## Kinect vs Realsense
De realsense SDK werd niet meer ontwikkeld dus zijn en was niet al te nauwkeurig dus wij hebben onderzoek gedaan naar alternatieve software en cameras. Ik heb zelf onderzoek gedaan naar software voor de Kinect camera. Ik heb hiervoor een open source versie alternatief voor de officïele Microsoft SDK gevonden namelijk Freenect. Daarnaast heb ik OpenNI2 en NITE gevonden. Dit zijn stukjes open source software die helpen met het tracken en identificeren van skeleten bij mensen voor de Kinect camera. Hieronder is een afbeelding van de tracking met behulp van voorgenoemde software.

<img src=/images/Freenect_good_tracking.png width="400" height="400"> 

Uitendelijk zijn we verder gegaan met de officïele software van Microsoft omdat deze stabieler was en makkelijker om mee te werken.

## Verkrijgen van de data

Ik ben bij bijna alle opname momenten geweest voor het verkrijgen van de data. Bij sommige was stond ik erbij om te helpen en bij andere keren was ik degene die de laptop met de opname apparatuur bediende. Ik was bij de volgende opnames erbij:

*Opnames in het atrium.
*Opnames in het zuiderpark.
*Opnames in het lokaal zelf van mensen die op ons af kwamen als reactie op een oproep van ons.
