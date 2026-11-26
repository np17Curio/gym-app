# Mijn gym app

Webapp om mijn gymschema, zwemtrainingen en lichaamsgewicht bij te houden.
Werkt offline en kan via Safari → Deel → "Zet op beginscherm" als app op de iPhone.

## Schema
- **Maandag en woensdag:** zwemmen
- **Dinsdag:** gym, training A
- **Donderdag:** gym, training B
- **Vrijdag tot en met zondag:** rustdagen

Bij het openen staat de app op het onderdeel van vandaag: op maandag en woensdag op **Zwemmen**, op de andere dagen op **Gym**.

Het gymschema loopt in blokken van 3 weken. Je doet 3 weken dezelfde oefeningen en die worden elke week iets zwaarder. Daarna volgt een nieuw blok met andere oefeningen. Na blok 3 begint blok 1 opnieuw. Het schema begint op maandag 23 november 2026 met blok 1, week 1.

## Wat de app kan

### Gym
- Je ziet per oefening de doelsets en de rusttijd, met de spieren die je traint.
- Je vult per set kilo's en herhalingen in en vinkt de set af. Na het afvinken start de rusttimer vanzelf.
- Het gewicht van de vorige keer is alvast ingevuld. Je krijgt ook een tip: zwaarder, hetzelfde gewicht houden of meer herhalingen.
- Je kunt een opwarmset bijhouden, en een warming-up en cooling-down afvinken.
- Je wisselt zelf tussen training A en B en tussen blok 1, 2 en 3.
- Met het **datumveld** vul je een training in voor een andere dag, ook achteraf. Kies je een dag die je al hebt opgeslagen, dan opent de app die training, zodat je hem kunt aanpassen.
- Na het opslaan zie je welke oefeningen je zwaarder of beter hebt gedaan dan de vorige keer.

### Zwemmen
- Je vult het aantal banen, de lengte van het bad, de tijd, de datum en eventueel een notitie in.
- De app rekent je meters en je tempo per 100 meter uit.
- Je ziet een overzicht per week, met de vergelijking met de week ervoor.

### Dag overslaan
- Op **Gym** en **Zwemmen** kun je de dag van vandaag overslaan. Je kiest dan een reden: **Ziek**, **Geen tijd** of **Geen zin**.
- Met **Toch trainen** of **Toch zwemmen** draai je het overslaan terug.

### Streak
- De streak telt je trainingsdagen op rij. Je ziet hem rechtsboven in de kop.
- Elke dag waarop je gymt of zwemt telt +1.
- Mis je een vaste dag (ma, di, wo of do), dan begint je streak weer bij 0. Overslaan met **Geen zin** telt ook als gemist.
- Sla je over met **Ziek** of **Geen tijd**, dan blijft je streak staan.
- Rustdagen breken je streak niet. Train je toch op een rustdag, dan telt die dag mee.
- Vandaag telt pas mee als je hebt getraind, maar breekt je streak ook niet zolang de dag nog bezig is.

### Geschiedenis
- **Streak:** je streak van nu, je record en een kalender van de laatste 4 weken.
- **Voortgang:** een grafiek van je zwaarste gewicht per oefening.
- **Overgeslagen:** hoe vaak je hebt overgeslagen, per reden.
- **Alle dagen op datum:** je gymtrainingen met de kilo's en herhalingen per set, je zwemtrainingen en de dagen die je hebt overgeslagen.
- **Backup:** maak een backup of zet er een terug.

### Mijn gewicht
- Je houdt je lichaamsgewicht bij, met een grafiek, het verschil sinds je start en een gemiddelde over 7 dagen.

## Bestanden
- `index.html`: de app
- `manifest.webmanifest`: naam, kleuren en icoon van de app
- `sw.js`: service worker, zorgt dat de app offline werkt
- `icon-180.png`, `icon-192.png`, `icon-512.png`: app-iconen

## Gegevens
Alles wordt opgeslagen op het apparaat zelf (localStorage), niet in deze map.
Maak af en toe een backup via **Geschiedenis → Backup**. In de backup zitten je gymtrainingen, zwemtrainingen, overgeslagen dagen en gewicht.

## Updaten
Pas je `index.html` aan? Verhoog dan ook `VERSION` in `sw.js` (bijvoorbeeld van `gym-v4` naar `gym-v5`).
Anders kan de iPhone de oude versie blijven tonen.
