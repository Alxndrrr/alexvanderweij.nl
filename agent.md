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
- Het adres `hoi@alexvanderweij.nl` wordt via de bestaande JavaScript-opbouw als zichtbare link en `mailto:` ingesteld.

Vervolgens verfijnd:

- De sectiekop is gewijzigd van `Email` naar `Contact`.
- De contactkop staat recht.
- De e-mailkaart is licht schuin gezet.
- Het envelop-icoon staat niet meer in een eigen boxed vlak.
- De e-mailkaart heeft extra grain in de achtergrond gekregen.

Daarna zijn de twee gestippelde connectorlijnen korter gemaakt, inclusief de mobiele hoogte.

De grain van de e-mailkaart is op mobiel rustiger gemaakt met grotere grain-tegels en een lagere overlay-opacity, zodat hij visueel dichter bij desktop ligt.
