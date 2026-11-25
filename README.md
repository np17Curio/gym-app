# Mijn gym app

Webapp voor mijn gymschema (in blokken van 3 weken), zwemtrainingen en lichaamsgewicht.
Werkt offline en kan via Safari → Deel → "Zet op beginscherm" als app op de iPhone.

## Bestanden
- `index.html`: de app
- `manifest.webmanifest`: naam, kleuren en icoon van de app
- `sw.js`: service worker, zorgt dat de app offline werkt
- `icon-180.png`, `icon-192.png`, `icon-512.png`: app-iconen

## Gegevens
Alles wordt opgeslagen op het apparaat zelf (localStorage), niet in deze repository.
Maak af en toe een backup via **Geschiedenis → Backup**.

## Updaten
Pas je `index.html` aan? Verhoog dan ook `VERSION` in `sw.js` (bijv. `gym-v2`),
anders kan de iPhone de oude versie blijven tonen.
