# Atlasjagd

Ein Geografie-Quiz für den Browser – optimiert fürs Handy, funktioniert aber auch am Desktop.

## Spielmodi

**Länder:** Land finden · Land benennen · Silhouette · Border Hop
**Flaggen & Hauptstädte:** Flagge auf Karte · Flaggen-Quiz · Hauptstädte
**Natur & Kultur:** Flüsse · Berge & Gebirge · Wahrzeichen

Formate: 10 Fragen, Auf Zeit, 3 Leben, Endlos, Schwächen.
Regionen: Welt, Europa, Afrika, Asien, Nordamerika, Südamerika, Ozeanien.

## Features

- **Clever wiederholen:** Für jedes Land und jede Fähigkeit (Lage, Flagge, Hauptstadt, Umriss, …) wird ein Lernstand gespeichert. Unbekanntes kommt oft, Gewusstes kaum noch.
- **Mein Atlas:** Fortschrittskarte; Länder lassen sich als „gewusst“ markieren.
- **Duelle:** Zu zweit auf einem Handy (gleiche Fragen nacheinander) oder per Duell-Code auf zwei Handys.
- **Kartenstile:** Klassisch, Flaggen, Bunt, Kontinente, Nacht, Retro, Blindkarte.
- **Projektionen:** Natural Earth, Equal Earth, Mercator, Globus. Flache Karten sind endlos scrollbar.

Fortschritt, Rekorde und Einstellungen liegen im `localStorage` des Browsers – also pro Gerät und Browser.
Unter **Mein Atlas → Datensicherung** lassen sie sich als JSON-Datei exportieren und wieder importieren (Import führt zusammen, statt zu überschreiben).

## Veröffentlichen mit GitHub Pages

1. Neues Repository anlegen und den Inhalt dieses Ordners hochladen (`index.html` muss im Wurzelverzeichnis liegen).
2. **Settings → Pages → Build and deployment:** Source „Deploy from a branch“, Branch `main`, Ordner `/ (root)`.
3. Nach ein, zwei Minuten läuft das Spiel unter `https://<user>.github.io/<repo>/`.
4. Auf dem iPhone in Safari öffnen → Teilen → „Zum Home-Bildschirm“.

Lokal testen: `python3 -m http.server` im Ordner starten und `http://localhost:8000` öffnen.

## Aufbau

Alles steckt in einer einzigen `index.html`: Karten-, Flaggen- und Ortsdaten sind eingebettet.
Nur D3, topojson-client (beide per CDN) und die Schrift „Bricolage Grotesque“ (Google Fonts) werden nachgeladen –
für den ersten Start ist also eine Internetverbindung nötig.

Datenquellen und Lizenzen: siehe [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## Icons

- `apple-touch-icon*.png` – iOS-Home-Bildschirm (180/167/152/120 px, randlos und ohne Transparenz; iOS rundet die Ecken selbst ab)
- `ios-icon.svg` / `ios-icon-1024.png` – Vorlage in voller Auflösung
- `icon-192.png`, `icon-512.png` – Web-App-Manifest (maskable)
- `icon.svg` – Favicon im Browser-Tab
