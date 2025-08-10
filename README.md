# IRIS — Shake to Read (Web App, v3)

**Neu in v3**
- 🔊 **Sound** beim Kapitelwechsel (kurzer Beep, über WebAudio; nach erstem Tap aktiviert)
- 🎞️ **Card-Transitions** (rein/raus animiert)
- ⌨️ **Typewriter-Effekt** (Buchstabe-für-Buchstabe; abschaltbar per CODE: TYPE_MODE)
- Beibehaltener iOS-Permissions-Flow + Sensor-Debug (aus v2)

## Lokal testen
- `index.html` öffnen oder `python3 -m http.server 8080` starten
- Im iPhone-Safari öffnen → Overlay: „Bewegung erlauben“ → beim ersten Tap wird auch **Audio** aktiviert
- Weiter per **Schütteln**, **Tippen**, Buttons oder mit **Pfeiltasten** (Desktop)

## Deployment (GitHub + Vercel)
- Repo erstellen, Dateien pushen, auf Vercel als „Other“ deployen (Build Command leer, Output `/`) – HTTPS inklusive

## Konfiguration
- Shake-Empfindlichkeit: `SHAKE_THRESHOLD` (Default 18), Cooldown `SHAKE_COOLDOWN` (ms)
- Typewriter: `TYPE_MODE` = `"char"` oder `"word"`, `TYPE_SPEED` (ms pro Schritt)
