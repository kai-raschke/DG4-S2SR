# DG4-S2SR — Sentinel-2 Super-Resolution: Endergebnisse

Statische Präsentation der Endergebnisse eines Sentinel-2-Super-Resolution-Vergleichs.
Dieses Repository enthält ausschließlich den fertig exportierten, offline-fähigen
HTML-Bundle für GitHub Pages — die eigentliche Verarbeitungs-Pipeline liegt in
einem separaten, privaten Projekt.

**Live:** https://kai-raschke.github.io/DG4-S2SR/

## Inhalt

Verglichen werden drei Produkte über ein landwirtschaftliches Testfeld:

- **LQ** — Sentinel-2, natives 10 m Raster
- **SR** — Super-Resolution (OpenSR), 2.5 m Raster
- **HQ** — UAV-Referenzbefliegung (Ground Truth)

Die Oberfläche gliedert sich in drei Abschnitte:

1. **Super-Resolution** — Kachel-Vergleich LQ/SR/HQ je Vegetationsindex (NDVI, EVI, LCI)
   und Termin, inkl. Zeitraffer und räumlicher Struktur (Moran's I).
2. **Statistik** — gepaarte Genauigkeit (Pearson r, MAE, RMSE) von SR bzw. LQ gegen die
   UAV-Referenz, aggregiert und je Termin.
3. **Baumreihen** — Querschnittsprofile quer über die Feld-Alleen zur Sichtbarmachung
   von Randeffekten an den Baumreihen.

## Lokale Nutzung

Das Bundle ist vollständig offline lauffähig — `index.html` einfach im Browser öffnen
(die `previews/`-Unterordner muss dabei erhalten bleiben).

## Lizenz

MIT, siehe [LICENSE](LICENSE).
