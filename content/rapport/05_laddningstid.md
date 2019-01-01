---
---
Laddningstid
=========================

Analys av webbplatsers laddningstid och användbarhet.

Urval
-----------------------


I denna rapport kommer olika webbplatsers laddningstid och användarbarhet att analyseras. Webbsidorna är olika kommuners hemsidor. Följande är valda för analys.

[__https://www.karlskrona.se__](https://www.karlskrona.se/) - Karlskrona kommuns hemsida.

[__https://www.ronneby.se__](https://www.ronneby.se/) - Ronneby kommuns hemsida.

[__http://solvesborg.se__](http://solvesborg.se/) - Sölvesborg kommuns hemsida.



Metod
-----------------------

Laddningstid för varje webbplats kommer att mätas via devtools och filken “Network”. Ett genomsnitt av tre laddningstider per hemsida kommer att presenteras. Sidorna kommer att testas med hjälp av [__PageSpeed Insights__](https://developers.google.com/speed/pagespeed/insights/) för att få fram ett resultat i form av poäng beroende på laddningstid, både för mobila enheter samt för desktop. Bilder på webbplatserna kommer att granskas för att se vilken storlek och de har och hur stor mängd data hela startsidan har.

[Alla mätresultat finns här](https://docs.google.com/spreadsheets/d/1Ffmh4Do6mlGD-tf81b0xWe7Xmg8wcbSWx-PsfO5wYCM/edit?usp=sharing)

Resultat
-----------------------

[__https://www.karlskrona.se__](https://www.karlskrona.se/)

<a href="image/karlskrona.png"><img src="image/karlskrona.png" alt="Karlskrona kommun"></a>

Karlskrona kommuns hemsida har en bild som bakgrund överst på första sidan som i stort består av en sökfunktion. Man kan tro att det är den som är största bilden till datamängd men det är en av de andra mindra bilderna som är större i KB räknat. Översta bilden är 337 KB stor. Bilden som är en länk till http://www.visitkarlskrona.se/sv är 600 KB stor.

Mätresultat. Snitt av tre sidladdningar och avrundade resultat.
<table>
<tr>
<td>Laddninstid i snitt: 3.29 sekunder
</tr>
<tr>
<td>Förfrågningar skickade: 59 stycken
</tr>
<tr>
<td>Total data överförd: 2.6 MB
</tr>
<tr>
<td>Lighgthouse mobil poäng: 44
</tr>
<tr>
<td>Lighgthouse dator poäng: 98
</tr>
</table>

-------

[__https://www.ronneby.se__](https://www.ronneby.se/)

<a href="image/ronneby.png"><img src="image/ronneby.png" alt="Ronneby kommun"></a>

Ronneby kommuns hemsida har väldigt få bilder. Den har samma upplägg som Karlskronas med en bakgrundsbild övers på sidan där det finns en sökruta. Längre ner finns en bild i ett reklam och nyhetsflöde. Bakgrundsbilden verkar slumpas fram och de är av olika storlek. Sidan har laddats om flertalet gånger för att se hur stora bilderna är datamässigt. Den minsta som visas under testen som gjordes är 188 KB stor och den största bilden är 339 KB stor.

<table>
<tr>
<td>Laddninstid i snitt: 2.42 sekunder
</tr>
<tr>
<td>Förfrågningar skickade: 100 stycken
</tr>
<tr>
<td>Total data överförd: 1.2 MB
</tr>
<tr>
<td>Lighgthouse mobil poäng: 28
</tr>
<tr>
<td>Lighgthouse dator poäng: 98
</tr>
</table>

-------

[__http://solvesborg.se__](http://solvesborg.se/)

<a href="image/solvesborg.png"><img src="image/solvesborg.png" alt="Sölvesborg kommun"></a>

Sölvesborg kummuns hemsida har likt de andra två en bild övers på sidan där det finns en sökfunktion. På denna sidan är det ett bildspel som går runt. Det är stora bilder på över en MB per bild. Sidan går snabbt att ladda trots att det är 8 MB som överförs.


<table>
<tr>
<td>Laddninstid i snitt: 2.36 sekunder
</tr>
<tr>
<td>Förfrågningar skickade: 44 stycken
</tr>
<tr>
<td>Total data överförd: 8.0 MB
</tr>
<tr>
<td>Lighgthouse mobil poäng: 44
</tr>
<tr>
<td>Lighgthouse dator poäng: 94
</tr>
</table>

Analys
-----------------------

För samtliga sidor tycker jag det går snabbt att ladda sidan. Vid flera tester kunde det noteras att det kunde skilja en del. Testerna är gjorda från hemmet där annan utrustning nyttjar samma bandbrädd vilket möjligen kan påverkat resultatet. Alla mobila enheter samt IP-TV använder samma bandbrädd. Det som jag tycker sticker ut i resultatet är Sölvesborgs sida som laddar hela 8 MB men går ändå snabbast att ladda. Den sidan skickar minst antal förfrågningar, mindre än hälften vad Ronneby skickar. När man kollar i DevTools kan man inte se de stora bilderna men kollar man på bildadressen så är det Sölvesborgs bilder från bildspelet som är stora. De ser ut att ligga i ett bild-script som kanske snabbar på det hela. Kanske bara laddar den bild som ska visas.
För att kunna minsta laddningstiden skulle man t.ex. i Karlskronas fall kunna använda en bild med lite sämre kvallité som sin länk till Turistbyrån, då den är ganska liten till ytan men ändå 600 KB stor.
Lösningen Sölvesborg använder verkar spara in mycket för sitt bildspel. Möjligen kan man använda jpg med något sämre kvallité.
Ronneby skickar många förfrågningar. Vilket påverkar poängen för mobila enheter markant. Ronnebys sida består av minst data men får lägst betyg mobilt. Renderingen blockeras av resurser. Kan man lägga dem sist så att bilder och tesxt kan renderas snabbare kan man kanske få bättre betyg.
Samtliga sidor får fram bilden överst på sidan samt sökfunktionen väldigt snabbt vilket jag tror är det viktigaste. Får man fram hela sidan på under 4 sekunder är det bra och det vesentliga visas mycket snabbare än så på samtliga sidor i rapporten.

Som vinnare i denna rapport utses Sölvesborg.
Ganska jämnt med Karlskrona men att få ut så mycket data och ändå ladda så pass snabbt avgör i detta fall.


Referenser
-----------------------

[Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/)

[PageSpeed Insights (Lighthouse)](https://developers.google.com/speed/pagespeed/insights/?hl=sv)

Övrigt
-----------------------

Rapport skriven av Magnus Danielsson
