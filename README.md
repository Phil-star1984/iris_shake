# IRIS — Shake to Read (Web App)

Eine minimalistische, terminal-inspirierte Web App, die die Story **IRIS** kapitelweise erzählt.
Auf dem **iPhone** kannst du zum nächsten Kapitel **schütteln**. Alternativ tippst du auf den Bildschirm.

## Features
- 15 kurze Kapitel-Screens (optimiert für Smartphones)
- **Shake-to-next** via DeviceMotion (mit iOS-Permission Overlay)
- Fallback: **Tippen**, **Buttons** und **Tastatur** (für Desktop-Test)
- Linux/Terminal/Hacker-Ästhetik (monospace, scanlines, neon green)
- Speichert Fortschritt in `localStorage`

## Lokal testen
1. Lade die Dateien herunter und öffne `index.html` direkt im Browser **oder** starte einen lokalen Server:
   ```bash
   python3 -m http.server 8080
   # dann im Browser: http://localhost:8080
   ```

## Deploy auf GitHub + Vercel
1. Neues Repo anlegen und Dateien pushen:
   ```bash
   git init
   git add .
   git commit -m "IRIS shake-to-read initial"
   git branch -M main
   git remote add origin <DEIN_REPO_URL>
   git push -u origin main
   ```
2. Auf **vercel.com** einloggen → **New Project** → dein Repo auswählen → Framework: **Other** → Build Command: _(leer)_ → Output: `/` (root).
3. Deploy. Fertig.

## Kapitel anpassen
- Öffne `index.html` und suche das Array `chapters`. Texte bearbeiten, Reihenfolge ändern oder weitere Kapitel ergänzen.
- Threshold für Shake anpassen: `SHAKE_THRESHOLD` (Default 20). Höher = stärker schütteln nötig.

## Hinweise
- Auf iOS (Safari) muss per Button zuerst **Bewegung erlaubt** werden. Ohne Erlaubnis kannst du weiterhin per **Tippen** blättern.
- Manche Desktop-Browser liefern kein `devicemotion`; das ist normal. Nutze Pfeiltasten oder Maus.
