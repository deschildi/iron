# IRON – dein Gym-Tracker

Eine einfache Web-App fürs iPhone: Sätze erfassen, Verlauf ansehen, Fortschritt als Grafik.
Läuft auch offline und hat ein eigenes Icon auf dem Homescreen.

## Dateien

| Datei | Wofür |
|---|---|
| `index.html` | Die ganze App: Aussehen (CSS) und Logik (JavaScript) |
| `manifest.webmanifest` | Name, Farben und Icons für den Homescreen |
| `sw.js` | Sorgt dafür, dass die App auch ohne Internet startet |
| `icons/` | Logo in allen Grössen, plus Startbild fürs iPhone 12 |

## Online stellen mit GitHub Pages (gratis, ca. 10 Minuten)

1. Auf [github.com](https://github.com) ein kostenloses Konto erstellen.
2. Oben rechts auf **+** → **New repository**. Name: `iron`, Sichtbarkeit **Public**, dann **Create repository**.
3. Auf der neuen Seite auf **uploading an existing file** klicken. Die ZIP-Datei auf dem Laptop entpacken und den *Inhalt* des Ordners (`index.html`, `sw.js`, `manifest.webmanifest`, `README.md` und den Ordner `icons`) ins Browserfenster ziehen. Dann **Commit changes**.
4. Im Repository auf **Settings** → **Pages**. Bei *Branch* `main` und `/ (root)` wählen, dann **Save**.
5. Nach 1–2 Minuten steht oben auf der Pages-Seite deine Adresse, z.B. `https://deinname.github.io/iron/`.

„Public“ heisst nur, dass der Code sichtbar ist. Deine Trainingsdaten landen nie auf GitHub.

## Aufs iPhone holen

1. Die Adresse in **Safari** öffnen (nicht Chrome).
2. Auf das Teilen-Symbol tippen (Quadrat mit Pfeil nach oben).
3. **Zum Home-Bildschirm** → **Hinzufügen**.

Ab jetzt startest du IRON über das Icon, im Vollbild und auch ohne Internet.

## Teilen

Jede Person, die den Link öffnet und zum Homescreen hinzufügt, hat ihre eigene App.
Die Trainings werden nur auf dem jeweiligen Handy gespeichert, niemand sieht die Daten der anderen.

## Backup

Unter **Mehr → Backup sichern** speicherst du eine Datei, z.B. in iCloud Drive.
Mit **Backup laden** holst du sie zurück, auch auf ein neues iPhone.
Wichtig: Wenn du IRON vom Homescreen löschst, sind auch die Daten weg. Vorher ein Backup machen.

## Später etwas ändern

1. `index.html` anpassen (oder Claude darum bitten).
2. In `sw.js` die Version erhöhen, z.B. `iron-v1` → `iron-v2`.
3. Die geänderten Dateien auf GitHub wieder hochladen.

Beim nächsten Öffnen mit Internet lädt die App die neue Version.

## Wie die Daten aussehen

Alles steht im Browser-Speicher unter dem Schlüssel `iron-data-v1`:

```json
{
  "exercises": ["Bankdrücken", "Kniebeugen"],
  "sets": [
    { "id": "lx3k9", "date": "2026-10-06", "t": 1791300000000, "ex": "Bankdrücken", "kg": 60, "reps": 8 }
  ],
  "current": "Bankdrücken"
}
```

Ein Training ist einfach alle Sätze mit demselben Datum.
