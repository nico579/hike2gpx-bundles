# hike2gpx bundles

This repository holds no code. It publishes the offline bundles of
[hike2gpx](https://github.com/nico579/hike2gpx): for each 5° BRouter cell, everything
the application needs to plan a hike without a network connection.

- the BRouter routing data (`.rd5`), with the national official paths merged into
  OpenStreetMap where OpenStreetMap lacks them (IGN BD TOPO in France);
- the map layers shown by the page (OSM paths, barriers, crossings, official paths);
- a manifest listing every file with its size and SHA-256.

Everything lives in a single release, [`bundles`](../../releases/tag/bundles), updated in
place every week, so its catalog keeps one stable address:

```
https://github.com/nico579/hike2gpx-bundles/releases/download/bundles/catalog.json
```

The bundles are built here by GitHub Actions, with the very code the desktop application
uses (`hike2gpx bundles`, see [its workflow](https://github.com/nico579/hike2gpx/blob/main/.github/workflows/bundles.yml)).
A bundle is rebuilt only when its OpenStreetMap extract or its official data has a newer edition.

## Data and licences

Each bundle carries its sources and attribution in its manifest:

- © OpenStreetMap contributors, [ODbL](https://opendatacommons.org/licenses/odbl/);
- BD TOPO © IGN, [Licence Ouverte Etalab 2.0](https://www.etalab.gouv.fr/licence-ouverte-open-licence/);
- elevation from [Mapterhorn](https://mapterhorn.com/attribution);
- routing by [BRouter](https://github.com/abrensch/brouter).

Les lots hors ligne de hike2gpx, refaits chaque semaine : un lot par case BRouter de 5°,
téléchargé et vérifié par l'application.
