# IRIS — Shake to Read (Web App, v4)

**Fixes für Sound auf iOS**
- Audio wird **bei erster Nutzer-Geste** (Tap/Click) initialisiert und gleich ein Test‑Blip gespielt
- Beep lauter & markanter (Square‑Wave, Envelope)
- Async `AudioContext.resume()` + Statusanzeige
- Sound wird auch beim Klick auf „Bewegung erlauben“ aktiviert

**Was bleibt:**
- Shake‑Navigation mit iOS‑Permission Overlay
- Animierte Kartenwechsel
- Typewriter‑Effekt (char/word, Speed konfigurierbar)
- Sensor‑Debug + Audio‑Status

## Tipp, falls weiterhin kein Sound:
- iPhone nicht im Stumm‑Schalter / Lautstärke hoch
- Safari nutzen (nicht In‑App‑Browser), normaler Modus
- Einmal **irgendeine Stelle tippen** (zum Freischalten), dann schütteln

## Lokal testen
```bash
python3 -m http.server 8080
# iPhone Safari öffnen → Overlay „Bewegung erlauben“ → tippen (Audio frei) → schütteln
```
