# 🗺️ Homburg im Saar LiDAR Explorer

Hier pflegen die **Ortspaten** von Homburg (Kreisstadt im Saarpfalz-Kreis, AGS 10045114, 82,6 km²), was der Explorer über ihren Ort zeigt: besondere Orte, Geschichten,
Riesenbäume, Pflanz- und Entsiegelungsaktionen und später eigene 3D-Zonen. Die Geländedaten (Laserscanning) baut
GitHub Actions aus offenen amtlichen Daten – sie liegen **nicht** in diesem Repository.

**Schauen, nicht graben.** Der Explorer zeigt Spuren im Gelände unter dem Wald: Wälle, Gräben, Gruben, Hohlwege.
Was er hervorhebt, sind *Hypothesen*, keine Funde. Bodendenkmäler sind gesetzlich geschützt (SDschG Saarland,
DSchG Rheinland-Pfalz): nicht graben, nicht sondeln, Funde der Denkmalpflege melden. Hinweise zum Graben oder auf
Kampfmittel werden hier nicht veröffentlicht.

## Mitmachen

- **Ohne Git:** ein [Issue](../../issues/new/choose) aufmachen – *Riesenbaum melden*, *Fehler melden*,
  *Aktion melden* oder *Geschichte vorschlagen*. Eine Ortspatin oder ein Ortspate macht daraus einen Beitrag.
- **Mit GitHub im Browser:** Datei anlegen oder ändern und einen Pull Request stellen. Die Prüfungen laufen
  automatisch; eine Ortspatin oder ein Ortspate schaut jeden Beitrag an.
- **Vorschau ohne Installation:** „Code → Codespaces → Create codespace“ öffnet eine fertige Umgebung; dort zeigt
  `werkzeuge/vorschau.sh` die Inhalte auf einer Karte.

Schritt für Schritt: [CONTRIBUTING.md](CONTRIBUTING.md).

## Was wo liegt

| Pfad | Inhalt |
|---|---|
| `ort.toml` | Steckbrief: Katalog-Id, Name, Gemeindeschlüssel, Ortspaten, Optionen (Relikt-Kandidaten, Punktwolken) |
| `inhalte/orte/*.geojson` | Besondere Orte als Punkte |
| `inhalte/geschichten/*.md` | Geschichten mit Kopf (Titel, Autor, Lizenz, Datum, Quellen) |
| `inhalte/bilder/` | Eigene Fotos (ohne EXIF) mit Bildangaben `<bild>.yml` |
| `aktionen/*.yml` | Pflanz-, Entsiegelungs- und Pflegeaktionen |
| `zones/` | 3D-Zonen – Schloss Karlsberg und Bäckerei Heusser liegen vorerst noch im Explorer-Daten-Repository, siehe `zones/README.md` |
| `werkzeuge/` | Prüfskript `ort_check.py`, Schemas, Vorschau |
| `.github/workflows/build.yml` | baut die Daten mit der festgelegten Pipeline-Version und veröffentlicht sie auf GitHub Pages |
| `.github/workflows/checks.yml` | Prüfungen bei jedem Pull Request |

Die veröffentlichten Daten liegen unter `https://open-kirrberg.github.io/ort-homburg/` (`manifest.json`); der
Explorer findet sie über den [Orte-Katalog](https://open-kirrberg.github.io/orte-katalog/catalog.json).
Ranglisten („Orte im Vergleich“) rechnet der Katalog zentral – ein Ort-Repository kann sie nicht beeinflussen.

## Lizenzen

Code MIT, Texte und Fotos CC BY 4.0 (oder CC BY-SA 4.0 je Beitrag), Datenbeiträge CC0 1.0 bzw. ODbL bei
OpenStreetMap-Ableitungen. Details und Quellen der Geländedaten: [LIZENZEN.md](LIZENZEN.md).

## Besonderheiten von Homburg

- **Relikt-Kandidaten sind an** (`relict_candidates = true`): Homburg war das erste Gebiet des Explorers; die
  öffentlichen Gesamtdaten zeigen die automatisch erkannten Kandidaten hier schon (ADR 0009, 0053).
  Es sind Hypothesen – Schauen, nicht graben.
- **Punktwolken** für drei Schwerpunkte: Schloss Karlsberg, Homburger Schlossberg (Hohenburg), Burgruine Merburg.
- **Zonen** Schloss Karlsberg und Bäckerei Heusser bleiben in der Übergangszeit im Daten-Repository
  `saar-lidar-data` ([zones/README.md](zones/README.md)).
