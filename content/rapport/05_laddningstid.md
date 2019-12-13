---
---
Kmom05 Laddningstid
=======================

Uppgiften går ut på att välja ut tre olika webbplatser och testa dem för att mäta hur snabbt de laddas och om de innehåller några saker som kan förbättras med tanke på laddningstid och användbarhet.

Urval
-----------------------
Jag har valt att analysera de officiella svenska webbsidorna för några biltillverkare. Man kan på förhand anta att en biltillverkare vill visa en mängd bilder på sina produkter och bilder kan ju potentiellt bli flaskhalsar i hur lång tid det tar att ladda in en webbsida. Av den anledningen tycker jag att det kan vara intressant att studera följande webbsidor:

1) [Audi](https://www.audi.se/se/web/sv.html)

2) [BMW](https://www.bmw.se/sv/index.html)

3) [Volvo Car](https://www.volvocars.com/se)

Metod
-----------------------
Metoden består i att studera sidornas prestanda genom att mäta deras laddningstid, antalet resurser som laddas och sidornas totala storlek i MB. De verktyg som används för detta är Lighthouse och Devtools i Firefox i fliken networks. "No throttling" används i dessa mätningar i Lighthouse.

Resultat
-----------------------

<h4>Mätvärden</h4>
Länk till Google Sheets: [Resultat mätningar]( https://docs.google.com/spreadsheets/d/1HWuktN6QJZquK9XAz9dGVuOEvyqHTrzb410KwEq0Z5M/edit?usp=sharing)


Audi
-----------------

[FIGURE src="image/audi.jpg?w=850" class="right" caption="Del av Audis hemsida"]

Audis sida upplevs som relativt snabb men har enligt Devtools sämst laddningstid. Det är dock inga stora skillnader mellan sidorna i absoluta tal. Pagespeed ger betygen 9 för mobilt och 42 för dator.


<h4>Förslag på förbättringar</h4>

<h5>Dator</h5>
* Skicka bilder i modernare bildformat
* Ta bort resurser som blockerar renderingen

<h5>Mobile</h5>
* Skjut upp inläsningen av bilder som inte visas på skärmen
* Skicka bilder i modernare bildformat
<br></br>

BMW
-----------------

[FIGURE src="image/bmw.jpg?w=850" class="right" caption="Del av BMW:s hemsida"]

BMW:s sida ger bäst betyg av de jämförda sidorna. Pagespeed ger betygen 11 för mobilt och 56 för dator. Den upplevs också som en aningen snabbare än Audis.


<h4>Förslag på förbättringar</h4>

<h5>Dator</h5>
* Ta bort resurser som blockerar renderingen
* Skicka bilder i modernare bildformat

<h5>Mobile</h5>
* Skicka bilder i modernare bildformat
* Ta bort oanvänd CSS
<br></br>


VOLVO
-----------------

[FIGURE src="image/volvo.jpg?w=850" class="right" caption="Del av Volvos  hemsida"]

Volvos sida får inget betyg av Pagespeed. Det står bara ett frågetecken för både dator och mobilt. Uppmätta värden på Devtools gör att sidan hamnar i mitten av jämförda sidor. Däremot upplevs sidan som långsammast då alla bilderna visas först efter flera sekunder på min dator. Detta verkar dock inte återspeglas av Devtools värden.

<h4>Förslag på förbättringar</h4>

<h5>Dator</h5>
* Ta bort resurser som blockerar renderingen
* Ta bort oanvänd CSS

<h5>Mobile</h5>
* Minska svarstiderna från servern (tid till första byte)
* Ta bort oanvänd CSS
<br></br>


Analys
-----------------------
Rent generellt bör bilder på webbsidor göras så små och komprimerade som möjligt. Detta är särskilt viktigt för biltillverkare då de ofta har många bilder på sina webbplatser. Dock inte så små eller med så låg upplösning att bilderna upplevs som suddiga eller grovkorniga. Det kan göras genom att använda moderna bildformat och att beskära bilderna. Vidare bör bilderna göras responsiva så att de görs mindre för mobila enheter.

En annan viktig aspekt är att tänka i vilken ordning resurser laddas in. Essentiella resurser bör laddas in först och sedan laddas resurser in då de används.

Av Pagespeed rekommenderade förbättringar är att "skicka bilder i modernare bildformat" "det vanligaste tipset följt av "ta bort resurser som blockerar renderingen".

Av de jämförda sidorna upplevs laddningstiden för Audis och BMW:s sidor vara i det närmaste identiska medan för Volvo tar det längre tid för hela sidan att laddas in. Detta återspeglas dock inte av de uppmätta värdena fullt ut.

Baserat på ovanstående, d v s både på mätvärden och upplevd hastighet, rankar jag BMW som vinnare tätt följd av Audi. Anledningen till att Volvo inte får något betygresultat i Pagespeed har inte kunnat i utrönas i denna starkt avgränsade studie.

Inköp av kapitalvaror som bilar, gör de flesta människor bara några gånger i livet. Det innebär att man kan stå ut med att webbsidor för kapitalvaror laddas lite längre tid än webbsidor för konsumtionsvaror. Om sidor för kapitalvaror tar längre tid än 6-7 sekunder är det för lång tid i mitt tycke. Alla jämförda sidor i studien klarar med marginal denna gräns. Webbupplevelsen på sidorna rent generellt är angenäm.   


Referenser
-----------------------

Litteratur:
The Principles of Beautiful Web Design av Jason Beaird (ISBN: 9780992279448). Kapitel 5.


Övrigt
-----------------------

Rapport skriven av Joakim Hellgren, student på Blekinge Tekniska Högskola.
