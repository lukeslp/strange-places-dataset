---
license: other
task_categories:
  - feature-extraction
language:
  - en
tags:
  - earth-science
  - geography
  - geospatial
  - natural-disasters
  - archaeology
  - ufo
  - meteorites
  - caves
  - tornadoes
  - earthquakes
  - volcanoes
  - ghost-towns
  - megaliths
  - shipwrecks
  - bigfoot
  - haunted-places
pretty_name: Strange Places v5.2 - Real-World Mysterious Phenomena
size_categories:
  - 100K<n<1M
dataset_info:
  features:
    - name: category
      dtype: string
    - name: latitude
      dtype: float64
    - name: longitude
      dtype: float64
    - name: name
      dtype: string
    - name: description
      dtype: string
    - name: date
      dtype: string
  splits:
    - name: train
      num_examples: 354770
---

# Strange Places v5.2

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE.md)
[![Records](https://img.shields.io/badge/Records-354%2C770-brightgreen)](https://github.com/lukeslp/strange-places-dataset)
[![Categories](https://img.shields.io/badge/Categories-14-blue)](https://github.com/lukeslp/strange-places-dataset)
[![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97-HuggingFace-yellow)](https://huggingface.co/datasets/lukeslp/strange-places-mysterious-phenomena)
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF)](https://www.kaggle.com/datasets/lucassteuber/strange-places-mysterious-phenomena)

354,770 georeferenced mysterious phenomena from NASA, NOAA, USGS, BFRO, NUFORC, OpenStreetMap, the Megalithic Portal, and the Shadowlands Haunted Places Index. Every record comes from authoritative databases -- no synthetic data.

Part of the [Data Trove](https://dr.eamer.dev/datavis/data_trove/) collection at [dr.eamer.dev](https://dr.eamer.dev).

## What's Inside

- 354,770 records across 14 categories
- 99.9% valid coordinates (354,544 georeferenced)
- Balanced: largest category is 20%
- All real data from government and authoritative sources
- Global coverage

## Categories

| Category | Count | Source |
|----------|-------|--------|
| Tornadoes | 71,813 | NOAA |
| Caves | 70,242 | OpenStreetMap |
| UFO Sightings | 60,632 | NUFORC |
| Megalithic Sites | 60,028 | Megalithic Portal |
| Meteorite Landings | 32,186 | NASA |
| Ghost Towns | 18,154 | OpenStreetMap |
| Storm Events | 14,770 | NOAA |
| Haunted Places | 9,717 | Shadowlands Index |
| Thermal Springs | 5,003 | NOAA |
| Bigfoot Sightings | 3,797 | BFRO |
| Earthquakes | 3,742 | USGS |
| Shipwrecks | 3,653 | NOAA |
| Fireballs | 863 | NASA |
| Volcanoes | 170 | USGS |

## Visualizations

I built several interactive visualizations using this data:

- [**Keep Looking**](https://dr.eamer.dev/datavis/poems/keep-looking/) -- a visual poem about UFO sightings and wonder
- [**Strange Places Explorer**](https://dr.eamer.dev/datavis/interactive/strange-places/) -- interactive map of all phenomena
- [**Big Foot**](https://dr.eamer.dev/datavis/poems/bigfoot/big-foot.html) -- BFRO sighting patterns

## Record Format

```json
{
  "category": "bigfoot_sightings",
  "latitude": 47.7511,
  "longitude": -120.7401,
  "name": "Report 637: Campers' encounter in Wrangell - St. Elias",
  "description": "Class A - Witnesses observed a large bipedal figure...",
  "date": "2000-06-16"
}
```

## Usage

```python
import json

with open('strange_places_v5.2.json') as f:
    data = json.load(f)

print(f"Total: {len(data):,} records")

# Filter by category
bigfoot = [r for r in data if r['category'] == 'bigfoot_sightings']
ghosts = [r for r in data if r['category'] == 'haunted_places']
```

## Sources & Licenses

| Source | Categories | License |
|--------|-----------|---------|
| NASA | Meteorites, Fireballs | Public Domain |
| NOAA | Tornadoes, Storms, Springs, Shipwrecks | Public Domain |
| USGS | Earthquakes, Volcanoes | Public Domain |
| OpenStreetMap | Caves, Ghost Towns | ODbL 1.0 |
| Megalithic Portal | Megalithic Sites | Attribution |
| NUFORC | UFO Sightings | Fair Use |
| BFRO | Bigfoot Sightings | Fair Use |
| Shadowlands Index | Haunted Places | Fair Use |

## Versions

- **v5.2** (2026-02): Added bigfoot sightings (BFRO, 3,797) and haunted places (Shadowlands, 9,717). 354K records, 14 categories.
- **v5.1** (2026-01): Removed waterfalls (separate dataset), 341K records
- **v5.0** (2025-12): Added storm events, thermal springs
- **v4.0** (2025-11): Initial release

## Related

- [Data Trove](https://dr.eamer.dev/datavis/data_trove/) -- full dataset catalog
- [lukesteuber.com](https://lukesteuber.com) -- portfolio
- [Kaggle](https://www.kaggle.com/datasets/lucassteuber/strange-places-mysterious-phenomena)
- [HuggingFace](https://huggingface.co/datasets/lukeslp/strange-places-mysterious-phenomena)

## Author

[Luke Steuber](https://lukesteuber.com) -- [@lukesteuber.com](https://bsky.app/profile/lukesteuber.com) on Bluesky

## Structured Data (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Dataset",
  "name": "Strange Places v5.2 - Mysterious Phenomena",
  "description": "354,770 mysterious phenomena worldwide including UFO sightings, bigfoot sightings, haunted places, megaliths, caves, ghost towns, meteorites, fireballs, tornadoes, earthquakes, volcanoes, and shipwrecks from NASA, NOAA, USGS, BFRO, NUFORC, OpenStreetMap, Shadowlands, and the Megalithic Portal.",
  "url": "https://www.kaggle.com/datasets/lucassteuber/strange-places-mysterious-phenomena",
  "sameAs": "https://huggingface.co/datasets/lukeslp/strange-places-mysterious-phenomena",
  "license": "https://creativecommons.org/licenses/by/4.0/",
  "creator": {
    "@type": "Person",
    "name": "Luke Steuber",
    "url": "https://lukesteuber.com"
  },
  "keywords": ["UFO", "bigfoot", "haunted places", "caves", "megaliths", "ghost towns", "meteorites", "earthquakes", "volcanoes", "tornadoes", "geospatial", "mysterious phenomena"],
  "temporalCoverage": "1950/2026",
  "spatialCoverage": {
    "@type": "Place",
    "name": "Global"
  },
  "distribution": [
    {
      "@type": "DataDownload",
      "encodingFormat": "application/json",
      "contentUrl": "https://www.kaggle.com/datasets/lucassteuber/strange-places-mysterious-phenomena"
    }
  ]
}
```
