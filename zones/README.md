# 3D-Zonen von Homburg

Homburg hat zwei Zonen, die der Explorer schon zeigt:

| Zone | Quelle (Explorer-Repository) | Veröffentlicht in |
|---|---|---|
| Schloss Karlsberg (Rekonstruktion 1789) | `zones/schloss-karlsberg/` | `Open-Kirrberg/saar-lidar-data` → `zones/schloss-karlsberg/` |
| Bäckerei Heusser (Gebäude-Zwilling) | `zones/baeckerei-heusser/` | `Open-Kirrberg/saar-lidar-data` → `zones/baeckerei-heusser/` |

**Sie bleiben vorerst dort** (Plan „Orte skalieren“, S3, Entscheidung D8): Während der Übergangszeit liefert der
Explorer die Zonen weiter aus dem Daten-Repository `saar-lidar-data` aus, das so lange online bleibt. Der Umzug
hierher ist ein eigener Schritt, wenn der Zonen-Vertrag (`docs/zone-contract.md`, `sle-zone-v1`) Zonen aus
Ort-Repositories laden kann; dann zieht auch die Lizenz- und Datenschutzprüfung der Zonen mit (Schloss: ADR 0048,
Bäckerei: ADR 0042–0047, Zustimmung der Eigentümer).

Bis dahin: keine Zonen-Dateien in diesen Ordner legen.
