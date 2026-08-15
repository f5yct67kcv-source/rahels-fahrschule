# Rahels Fahrschule

Website für Rahels Fahrschule in Gelterkinden BL. Fahrstunden Kategorie B und Verkehrskundeunterricht.

## Aufbau

Statisches HTML, kein Framework, keine Abhängigkeiten, kein Build-Schritt.

- `index.html` – die ganze Seite, CSS und Skript liegen inline im Dokument
- `impressum.html`, `datenschutz.html` – Rechtsseiten, teilen sich `assets/seite.css`
- `assets/fonts/` – Switzer und Kaushan Script, lokal eingebunden
- `favicon.svg` – das L-Schild

Keine Cookies, keine Analyse-Werkzeuge, keine Aufrufe an fremde Server.

## Lokal ansehen

```bash
python3 -m http.server 8742
```

Dann http://localhost:8742 öffnen.

## Terminanfrage

Das Formular schickt nichts an einen Server. Es setzt aus den Eingaben eine fertige Nachricht zusammen und öffnet damit WhatsApp oder das Mailprogramm. Abgeschickt wird von Hand.

Der Abschnitt ist in der Grösse und Gestaltung gebaut, die ein Buchungswerkzeug später einnimmt. Geplant ist Cal.com mit Bestätigungspflicht, angeschlossen an Rahels eigenen Handykalender. Kommt es dazu, muss vorher `datenschutz.html` angepasst werden, weil dann tatsächlich Termine gespeichert werden.

## Vor dem Livegang

Die Seite ist bewusst aus der Suche genommen, solange sie nicht freigegeben ist.

1. In `index.html`, `impressum.html` und `datenschutz.html` die Zeile `<meta name="robots" content="noindex, nofollow">` entfernen
2. `robots.txt` durch die auskommentierte Freigabe am Dateiende ersetzen
3. `sitemap.xml` anlegen und in `robots.txt` verweisen
4. Kanonische Adresse und `og:url` in `index.html` eintragen

## Offen

- **Preise.** Fahrlektion, Mehrfachabo und VKU stehen als sichtbare Lücke auf der Seite. Sobald die Zahlen bestätigt sind, kommen sie in den Abschnitt `#preise`.
- **Foto.** Eine einzige Bildfläche, im Hero, hochformatig 4:5. Gebraucht wird ein Porträt von Rahel, auf dem sie klar die Hauptperson ist, am oder beim Auto, bei Tageslicht. Kein Text ins Bild, der steht darüber. Zweitwichtigstes Motiv wäre eine Fahrsituation von der Beifahrerseite. Keine KI-Bilder.
- **Impressum.** Postadresse, allfällige UID und Rechtsform fehlen, bis entschieden ist, was davon öffentlich stehen soll.
- **Datenschutz.** Der Hosting-Anbieter ist im Text noch nicht benannt.
- **Logo.** Lenkrad, Wortmarke und Schreibschrift sind aus den Fotos der Autobeschriftung nachgebaut, das Lenkrad als SVG, die Schrift gesetzt. Taucht die originale Vektordatei des Beschrifters auf, wird das Lockup ersetzt.
