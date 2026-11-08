# Bankroll & P/L Tracker – iPhone-PWA

## Kostenlos auf GitHub Pages veröffentlichen

1. Auf github.com anmelden (oder kostenloses Konto erstellen).
2. Neues Repository über **+ → New repository** erstellen, z. B. `bankroll-tracker`. **Public** auswählen (GitHub Pages ist bei GitHub Free für öffentliche Repositories verfügbar). Das Repository selbst enthält **keine persönlichen Wettaufzeichnungen**.
3. Die **Dateien aus diesem ZIP** hochladen: `index.html`, `manifest.webmanifest`, `sw.js` und den kompletten Ordner `icons` mit den zwei PNG-Dateien. Die Dateien müssen im Stammverzeichnis liegen. Auf GitHub: **Add file → Upload files → Commit changes**. ZIP nicht als einzelne Datei hochladen.
4. Im Repository **Settings → Pages → Build and deployment** öffnen. Unter **Source** `Deploy from a branch` auswählen, unter **Branch** `main` und `/ (root)` auswählen und **Save** drücken.
5. Warten, bis GitHub die Adresse unter **Settings → Pages** anzeigt. Sie lautet normalerweise `https://BENUTZERNAME.github.io/bankroll-tracker/` (abhängig von deinem Repository-Namen).
6. Diese Adresse auf dem iPhone in **Safari** öffnen. Auf **Teilen → Zum Home-Bildschirm → Hinzufügen** tippen. Starte die App anschließend über das neue Symbol.
7. Öffne die App mindestens einmal mit Internetverbindung, damit der Offline-Cache geladen wird. Danach kannst du die App ohne Internet nutzen.

## Daten und Sicherung

- Einträge und Einstellungen bleiben ausschließlich im lokalen Speicher der jeweiligen Web-App-Installation (`localStorage`). GitHub erhält die Einträge nicht.
- **Wichtig:** Die installierte Home-Bildschirm-App kann einen anderen Speicherbereich als Safari verwenden. Trage Daten nach Möglichkeit erst **nach der Installation** ein.
- Nutze **Backup speichern** regelmäßig und bewahre die JSON-Datei in der Dateien-App oder einem selbst gewählten sicheren Speicherort auf. **Backup laden** ersetzt die aktuellen Daten nach Rückfrage.
- Daten können bei Geräteverlust, Löschen der Website-Daten oder Entfernen der App verloren gehen. Ein PWA-Cache ist keine Datensicherung.
- Updates: Dateien im Repository ersetzen. Bei Änderungen an `index.html` für sichere Aktualisierung den Cache-Namen in `sw.js` von `bankroll-pwa-v1` auf z. B. `bankroll-pwa-v2` erhöhen. Die App ggf. einmal online neu öffnen.

## Funktionsumfang

- Name/Spiel, Quote, Einsatz und Ergebnis (ausstehend, gewonnen, verloren)
- Profit/Loss, Trefferquote, ROI, Verlauf und offene Einsätze
- Startbankroll, monatliches Verlustlimit, Warnung bei hohen Einsätzen
- JSON-Backup mit Wiederherstellung und CSV-Export
- Keine Buchmacherverbindung, kein Benutzerkonto, keine externen Skripte

## Hinweis zur Bankroll

Die angezeigte Bankroll ist Startbankroll plus **abgerechnete** Gewinne/Verluste. Noch offene Einsätze werden separat ausgewiesen; es ist daher kein verbindlicher Kontostand beim Wettanbieter. Einzahlungen/Auszahlungen nach Start sind nicht separat erfasst. Das monatliche Verlustlimit bezieht sich auf den monatlichen **Nettoverlust** der abgerechneten Einträge.

**Datenschutz:** Der Programmcode ist bei einem öffentlichen Repository öffentlich. Keine Zugangsdaten oder persönlichen Daten in die GitHub-Dateien schreiben. Wetteinträge werden nur im lokalen Browser gespeichert und nicht automatisch synchronisiert.
