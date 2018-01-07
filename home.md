# PORTFOLIO
*Bram Slemmer, 14081563*
Code
Courses
Opdrachten
Presentaties
Scrum

### Week 1 data science

In de eerste week waren wij nog bezig met het orienteren op de minor. Het begon met het rondkijken op het internet naar bestaande papers over de mogelijkheden van diepte cameras. Daarnaast gingen wij ons bezig houden met het werkend krijgen van de Realsense camera die wij tot onze beschikking hadden. Er was meer support voor linux dan voor Windows voor de realsense camera en aangezien ik de enige was met Ubuntu op de laptop was ik de aangewezen persoon om de camera werkend te krijgen. 

<img src=/images/Printscreen_camera.png width="600" he3ght="300">

*het eerste beeld wat wij kregen was het beeld wat je hierboven ziet. Aan de rechterkant zie je het dieptebeeld wat wij kregen van het linkerbeeld*

### Week 2-3 data science

De volgende stap die wij namen was het opslaan en verwerken van de beelden die we hieruit kregen. Dit werd gedaan door de dieptes die we terugkregen van de camera uitgedrukt in het aantal centimeter aan afstand van de camera uit te schrijven naar de terminal en die output weer op te slaan in een csv bestand. Het resultaat was een groot bestand met allemal cijfers zoals hieronder.

![CSV beelden camera](/images/combined_frames_csv.png)

Deze beelden konden wij dan weer omzetten door een grijswaarde te geven aan de cellen op basis van de waarde in de cellen. Daardoor kregen wij een soort van visuele representatie op van wat wij opslaan. Dit resultaat is hieronder weergeven

![Greyscale image realsense](/images/Frame1.png)

Het probleem wat wij hier hadden was dat de camera niet erg nauwkeurig leek te zijn. Er zaten zoals hierboven te zien is veel gaten in de beelden die wij opnamen. Er was wel wat literatuur over dit probleem gepubliceerd maar nergens een oplossing voor dit probleem. Wij hebben nog zelf geprobeerd om dit op te lossen door een gemiddelde te nemen van een aantal frames wat wel een deel van de gaten liet verdwijnen of minder maakte maar de vraag was of dit wel genoeg was voor ons doel.

![Average greyscale image realsense](/images/Frame_average.png)

Daarnaast hebben wij zitten zoeken naar een manier om de joint van mensen te tracken op de beelden die wij opnemen. Helaas was de SDK die beschikbaar was al enige tijd niet meer verder ontwikkeld en heeft Intel de ontwikkelink hiervan compleet stop gezet. Daarnaast waren er ook verder geen duidelijke oplossingen om dit te doen.

### Week 4 data science

Door de ontdekkingen die wij hebben gedaan van de tracking software en de nauwkeurigheid van de Realsense camera hebben wij besloten om ook naar andere camera's te kijken. De bekendste camera en tevens degene die wij het meeste tegenkwamen in literatuur was de Microsoft Kinect camera. Na enig onderzoek vonden wij dat deze beter getest was dan de Realsense en dat de software hiervoor ook nog eens veel verder ontwikkeld was. Vandaar dat wij besloten hebben om een Kinect camera aan te schaffen en hiermee verder te gaan. 

Voor de Kinect camera zijn er ook veel mogelijke libraries beschikbaar om mee te werken. Wij hebben zitten kijken naar 2 alternatieven voor het opnemen en het tracken. Ten eerste hadden wij de officiële Microsoft SDK en daarnaast hadden wij ook nog een open source versie genaamd Freenect voor het gebruiken van de camera in combinatie met OpenNI2 en NITE voor het tracken van de joints. 


<img src=/images/Freenect_good_tracking.png width="400" height="400"> <img src=/images/Capture2.png width="400" height="400">

*Freenect tracking*
*Kinect SDK*

### Week 5 data science

Vanaf ongeveer week 4/5 ben ik een stuk minder vaak en lang op school geweest aangezien ik door overspannenheid veel minder kon werken. Dit was gelukkig over na de herfstvakantie maar dit heeft mij de komende paar weken wel veel tegengehouden. In week 5 heb ik dan ook veel minder gedaan dan dat ik had gewild. Deze week zijn wij in het atrium gaan staan met de Kinect camera en een aantal normale cameras om mensen op te nemen. Wij hadden een opstelling gemaakt vanuit waar wij de mensen konden filmen met de Kinect maar ook met de normale cameras om te kunnen valideren dat de resultaten die wij kregen van de Kinect ook klopten. De testopstelling zag eruit als volgt:

<img src=/images/opstelling.jpg width="500" height="500">

*De kinect camera zit vooraan. Die neemt een dieptebeeld op van voren en de Joint punten. Aan de onderkant en zijkant staat ook en camera die gebruikt worden voor valideren*
