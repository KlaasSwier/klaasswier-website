# Klaas Swier bedrijfswebsite

Statische bedrijfswebsite voor:

- VOF Klaas Swier Veehandel
- Vee- en Vleeshandel Klaas Swier B.V.
- Verwijzing naar Slagerij Islam Centrum B.V.

De website bestaat uit één HTML-bestand en een map met afbeeldingen. Er is geen database, pakketbeheer of buildstap nodig.

## Bestandsstructuur

```text
index.html
assets/
  logo-slagerij.png
  logo-vleeshandel.png
  logo-vof.png
  swier-hero-v3.webp
vercel.json
```

## Lokaal controleren

Open `index.html` rechtstreeks in een browser. Voor een lokale webserver kan vanuit deze map ook worden uitgevoerd:

```bash
python -m http.server 8080
```

Open daarna `http://localhost:8080`.

## Publiceren via Vercel

1. Maak in GitHub een aparte repository, bijvoorbeeld `klaasswier-website`.
2. Upload alle bestanden en de volledige map `assets` naar de hoofdmap van die repository.
3. Kies in Vercel **Add New > Project** en importeer deze repository.
4. Kies bij Framework Preset **Other**.
5. Laat Build Command leeg en gebruik `.` als Output Directory als Vercel daarom vraagt.
6. Publiceer het project.
7. Voeg daarna in Vercel onder **Settings > Domains** het domein `klaasswier.nl` en eventueel `www.klaasswier.nl` toe.
8. Pas de DNS-records bij de domeinbeheerder aan volgens de waarden die Vercel toont.

Het bestaande Vercel-project van `uren.klaasswier.nl` blijft hierbij apart en hoeft niet te worden gewijzigd.

## Publiceren op een gewone webserver

Upload `index.html` en de map `assets` samen naar de openbare hoofdmap van `klaasswier.nl`, meestal `public_html`, `www` of `htdocs`. De mapstructuur moet hetzelfde blijven.

## Belangrijk voor de ICT-beheerder

- Doeldomein: `klaasswier.nl`
- Gewenste extra domeinnaam: `www.klaasswier.nl` doorsturen naar `klaasswier.nl`
- HTTPS/SSL inschakelen
- Oude website pas vervangen nadat deze versie op een tijdelijk adres is gecontroleerd
- Voor de overstap een back-up van de huidige website en DNS-instellingen maken
- `uren.klaasswier.nl` moet naar het bestaande urenregistratieproject blijven verwijzen

## Aanpassen

Alle inhoud, kleuren en werking staan in `index.html`. Afbeeldingen staan in `assets`. Na een wijziging volstaat een nieuwe commit; bij een gekoppeld Vercel-project wordt de website automatisch opnieuw gepubliceerd.
