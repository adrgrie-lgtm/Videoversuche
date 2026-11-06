# Videoschmiede

Musikvideo-Studio – komplett lokal im Browser. Verbesserte MuseGen-Vorlage.

## Was drin ist

- **index.html – VideoSchmiede:** Song + Material reinziehen → animiertes Musikvideo mit Intro/Outro und WebM-Export mit Ton.
  - **Foto-Serie-Modus:** Einzelbilder reinziehen, jedes Bild wird eine Filmszene (Ken-Burns-Kamerafahrten, weiche Blenden, Beat-Puls). Lange Songs bekommen automatisch mehrere Takes pro Bild.
  - **Visual-Stil-Modus (Neu):** Ganz ohne Bildmaterial zeichnen fünf audio-reaktive Stile – Neon-Grid, Partikel-Strom, Spektrum-Ring, Lo-Fi-Fenster, Cinematic – das Video live aus der Musik. Bass, Mitten und Höhen des Songs steuern Puls, Partikel, Regen, Licht und Platten-Drehung.
- **spalter.html – Collage-Spalter:** Collage (z. B. 4×6-Raster mit weißen Stegen) per Raster-Preset in Einzelbilder zerlegen – fertig für die VideoSchmiede. Jetzt auch als eigenes Repo: [Collage-Spalter](https://github.com/adrgrie-lgtm/Collage-Spalter).

## Workflow

1. Collage? Erst mit dem [Collage-Spalter](https://github.com/adrgrie-lgtm/Collage-Spalter) (hier: `spalter.html`) in Einzelbilder zerlegen.
2. `index.html` öffnen, Modus wählen: Foto-Serie oder Visual-Stil.
3. Musik (MP3/WAV/OGG/M4A) reinziehen, im Foto-Modus zusätzlich Einzelbilder, „Video zusammenbauen“ klicken.
4. „Video exportieren (WebM)“ – der Browser spielt das Video einmal durch und zeichnet es mit Ton auf.

Kein Server, kein Upload, kein Konto, kein Tracking – alles läuft lokal im Browser.

## KI-Feinschliff (November 2026, v2.5)

- **WebM-Dauer-Fix beim Export:** Die echte Spieldauer wird nach der Aufnahme direkt in den WebM-Header geschrieben – viele Spieler und Schnittprogramme melden sonst „unendliche“ Dauer und weigern sich.
- **Sinnvolle Export-Dateinamen:** songname.webm statt immer musikvideo.webm.
- **Schnellerer Visual-Stil „Partikel-Strom“:** Glow als wiederverwendetes Sprite statt Gradient pro Partikel und Frame – deutlich weniger Rechenlast, gerade beim Aufnehmen.
- **Filmkorn wechselt jetzt auch ohne Kamera-Zittern** korrekt zwischen den beiden Korn-Bildern.
- **Fortschrittsbalken friert nicht mehr ein**, wenn während der Wiedergabe gesucht und dann Play/Pause gedrückt wird.
- **Bedienung:** Suchleiste und Play-Button haben Aria-Labels (Screenreader).

## Videoclip-Szenen (November 2026, v2.6)

- **Videoclips als Szenen:** MP4/WebM-Clips (z. B. von FramePack, LTX-Video oder gratis Online-Generatoren) lassen sich jetzt genauso wie Bilder per Drag-and-drop laden – jeder Clip wird eine Filmszene.
- Der Clip läuft synchron zur Szenenzeit in der Timeline und loopt automatisch, wenn die Szene länger als der Clip ist.
- Clip-Szenen funktionieren mit allen Kameras (Ken-Burns, Kino-Kamera), Übergängen und Effekten wie Bild-Szenen.
- Thumbnails zeigen Clips mit "CLIP"-Badge; Mischen und Entfernen funktioniert identisch.
