# Wijzigingen

Op 21 juli 2026 zijn de scroll-gestuurde effecten uit `index.html` gehaald.

Gedaan:

- De introkaart is statisch gemaakt.
- Het sticky/fixed gedrag van de titel en introkaart is verwijderd.
- Het verkleinen/morphen van de introkaart tijdens scrollen is verwijderd.
- De clipping- en custom-property logica voor de introkaart is verwijderd.
- De pressure-line en bijbehorende placeholder-elementen zijn verwijderd.
- De scroll-gestuurde blur/reveal van de social links is verwijderd.
- De JavaScript scroll-handler, resize-meting en `requestAnimationFrame`-morphlogica zijn verwijderd.
- Het script onderaan doet nu alleen nog de e-mail-link omzetting.

Bewust laten staan:

- De gewone verticale connector tussen intro en socials.
- De zelfstandige `connector-drift` animatie van die connector, omdat die niet door scrollen wordt aangestuurd.

## Latere wijziging

Daarna is een aparte e-mailsectie onder `Socials` toegevoegd.

Gedaan:

- De e-mailrij is uit de social links verwijderd.
- Onder `Socials` is een nieuwe sectie `Email` toegevoegd.
- De nieuwe sectie is verbonden met dezelfde gestippelde verticale connector.
- Het aangeleverde envelop-icoon is toegevoegd als `assets/icons/email.svg`.
- De tekst `Even hoi zeggen? Stuur mij gerust een email` is toegevoegd.
- Het e-mailadres wordt via JavaScript opgebouwd, zonder het volledige adres als platte tekst in de HTML te zetten.

Vervolgens verfijnd:

- De sectiekop is gewijzigd van `Email` naar `Contact`.
- De contactkop staat recht.
- De e-mailkaart is licht schuin gezet.
- Het envelop-icoon staat niet meer in een eigen boxed vlak.
- De e-mailkaart heeft extra grain in de achtergrond gekregen.

Daarna zijn de twee gestippelde connectorlijnen korter gemaakt, inclusief de mobiele hoogte.

De grain van de e-mailkaart is op mobiel rustiger gemaakt met grotere grain-tegels en een lagere overlay-opacity, zodat hij visueel dichter bij desktop ligt.

De verticale spacing rond de gestippelde connectorlijnen is gelijkgetrokken met `--section-line-gap`, zodat de afstand van content naar lijn en van lijn naar volgende sectie in balans blijft op desktop en mobiel.

De volledige e-mailkaart is klikbaar gemaakt. De adresdelen staan licht gecodeerd in HTML en de echte `mailto:` wordt pas bij klikken opgebouwd.

Daarna zijn twee scroll-effecten teruggebracht:

- De naam bovenaan is weer sticky gemaakt en ligt visueel achter de introkaart.
- De naam wordt verborgen zodra de introkaart voorbij is, zodat hij niet onderaan opnieuw zichtbaar wordt.
- De twee gestippelde connectorlijnen schuiven tijdens scrollen visueel in elkaar en worden langer wanneer er terug omhoog wordt gescrold.
- De bolletjes blijven los van elkaar doordat de maximale krimp per lijn in JavaScript wordt begrensd.
- De scroll-updates lopen via `requestAnimationFrame` en respecteren `prefers-reduced-motion`.

Daarna is de connectoranimatie aangepast:

- De gestippelde lijn heeft nu een eigen inset ten opzichte van de bolletjes, zodat de lijn niet over de bolletjes heen loopt.
- Alleen de onderkant van de connector schuift omhoog; de bovenkant blijft staan.
- De krimp wordt aangestuurd door de positie van de eerstvolgende sectiekop, zodat het voelt alsof `Socials` en `Contact` de lijn omhoogduwen.
