# Bruchrechnen Klasse 6

Interaktive Lern-App zum Rechnen mit Brüchen für Schülerinnen und Schüler der 6. Klasse.

- Vier Reiter für Addieren, Subtrahieren, Multiplizieren und Dividieren, jeweils mit Merksatz, Alltagsbeispiel, Rechenweg, Ausprobieren und Übungsaufgaben in drei Stufen
- Zufällige Sachaufgaben mit Tipp-Funktion bei jeder Rechenart
- Reiter „Spiele“: Memory, Größer oder kleiner, Zeitjagd, Ganzes füllen
- Läuft im Browser ohne Server und ohne Anmeldung. Ergebnisse und Rekorde werden nur im jeweiligen Browser (localStorage) gespeichert
- Installierbar als App (PWA) und nach dem ersten Laden offline nutzbar

## Dateien

| Datei | Zweck |
| --- | --- |
| `index.html` | Die komplette App (HTML, CSS, JavaScript) |
| `manifest.webmanifest` | App-Name, Farben und Icons für die Installation |
| `sw.js` | Service Worker für den Offline-Betrieb |
| `icons/` | App-Icons |

## Lokal starten

Ein Service Worker läuft nur über `http://localhost` oder `https`, nicht über `file://`.

```
python3 -m http.server 8080
```

Danach `http://localhost:8080` öffnen.

## Veröffentlichen mit GitHub Pages

Der Workflow `.github/workflows/pages.yml` veröffentlicht die App bei jedem Push auf `main`.
Einmalig im Repository unter **Settings → Pages → Source** den Eintrag **GitHub Actions** wählen.

## Installieren

- **Android (Chrome):** Menü → „App installieren“
- **iPad/iPhone (Safari):** Teilen → „Zum Home-Bildschirm“
- **Windows, macOS, Linux (Chrome oder Edge):** Installieren-Symbol in der Adressleiste

## Neue Version ausliefern

In `sw.js` die Zahl bei `CACHE = 'bruchrechnen-v1'` erhöhen, damit der alte Offline-Cache ersetzt wird.

## Schriften

Die Schriften Baloo 2 und Nunito werden von Google Fonts geladen und danach im Cache abgelegt. Ohne Netz und ohne Cache nutzt die App Systemschriften.
