# DG4-S2SR — Sentinel-2 Super-Resolution: Endergebnisse

Statische Präsentation der Endergebnisse eines Sentinel-2-Super-Resolution-Vergleichs.
Dieses Repository enthält ein exportiertes HTML-Bundle für die Ergebnispräsentation.
Das Processing wird zeitnah in einem weiteren Repository veröffentlicht.

**Live:** https://kai-raschke.github.io/DG4-S2SR/

## Inhalt

Verglichen werden drei Produkte über das Versuchsfeld in Plotha.

- **LQ** — Sentinel-2, natives 10 m Raster
- **SR** — Super-Resolution (OpenSR/Sen2SR), 2.5 m Raster
- **HQ** — UAV-Referenzbefliegung (50 cm downsample der originalen Befliegungsdaten)

Die Oberfläche gliedert sich in drei Abschnitte:

1. **Super-Resolution** — Kachel-Vergleich LQ/SR/HQ je Vegetationsindex (NDVI, EVI, LCI)
   und Termin, inkl. Zeitraffer und räumlicher Struktur (Moran's I).
2. **Statistik** — gepaarte Genauigkeit (Pearson r, MAE, RMSE) von SR bzw. LQ gegen die
   UAV-Referenz, aggregiert und je Termin.
3. **Baumreihen** — Querschnittsprofile quer über die Feld-Alleen zur Sichtbarmachung
   von Randeffekten an den Baumreihen.

## Datenerzeugung und Herkunft

**Super-Resolution (SR).** Erzeugt mit den ESA-OpenSR-Modellen
[opensr-model](https://github.com/ESAOpenSR/opensr-model) (Latent-Diffusion, 10 m → 2.5 m)
und [SEN2SR](https://github.com/ESAOpenSR/SEN2SR) (20-m-Bänder). Zitation:

> Donike, S., Aybar, C., Gómez-Chova, L., & Kalaitzis, F. (2025). Trustworthy Super-Resolution
> of Multispectral Sentinel-2 Imagery With Latent Diffusion. *IEEE Journal of Selected Topics
> in Applied Earth Observations and Remote Sensing*, 18, 6940–6952.
> https://doi.org/10.1109/JSTARS.2025.3542220

```bibtex
@ARTICLE{ldsrs2,
  author={Donike, Simon and Aybar, Cesar and Gómez-Chova, Luis and Kalaitzis, Freddie},
  journal={IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing},
  title={Trustworthy Super-Resolution of Multispectral Sentinel-2 Imagery With Latent Diffusion},
  year={2025},
  volume={18},
  number={},
  pages={6940-6952},
  doi={10.1109/JSTARS.2025.3542220}}
```

**UAV-Daten (HQ-Referenz).** Bereitgestellt von der Martin-Luther-Universität
Halle-Wittenberg, Institut für Geowissenschaften und Geographie, Abteilungen
Geoökologie / Digitale Geographie, Deutschland.
Kontakt: https://insitu.geo.uni-halle.de/contact

**Sentinel-2-Daten (LQ).** Copernicus Sentinel-2 Missionsdaten, bezogen über die
[Copernicus Data Space Ecosystem](https://dataspace.copernicus.eu/data-collections/copernicus-sentinel-missions/sentinel-2).
Enthält modifizierte Copernicus-Sentinel-Daten, bereitgestellt von der ESA.

## Lizenz

MIT, siehe [LICENSE](LICENSE).
