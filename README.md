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
pretty_name: Strange Places v5.1 - Real-World Mysterious Phenomena
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
      num_examples: 341256
---

# Strange Places v5.1

341,256 mysterious phenomena from NASA, NOAA, USGS, OpenStreetMap, and the Megalithic Portal.

## What's Inside

- 341,256 records across 12 categories
- 99.9% valid coordinates (341,030 georeferenced)
- Balanced: largest category is 21%
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
| Thermal Springs | 5,003 | NOAA |
| Earthquakes | 3,742 | USGS |
| Shipwrecks | 3,653 | NOAA |
| Fireballs | 863 | NASA |
| Volcanoes | 170 | USGS |

## Record Format

```json
{
  "category": "caves",
  "latitude": 38.7749,
  "longitude": -122.4194,
  "name": "Crystal Cave",
  "description": "Limestone cave system",
  "date": "2023-01-15"
}
```

## Usage

```python
import json

with open('strange_places_v5.1.json') as f:
    data = json.load(f)

print(f"Total: {len(data):,} records")

# Filter by category
caves = [r for r in data if r['category'] == 'caves']
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

## Versions

- **v5.1** (2026-01): Removed waterfalls (separate dataset), 341K records
- **v5.0** (2025-12): Added storm events, thermal springs
- **v4.0** (2025-11): Initial release

## Distribution

- **Kaggle**: [lucassteuber/strange-places-mysterious-phenomena](https://www.kaggle.com/datasets/lucassteuber/strange-places-mysterious-phenomena)
- **HuggingFace**: [lukeslp/strange-places](https://huggingface.co/datasets/lukeslp/strange-places)
- **GitHub Gist**: [Demo Notebook](https://gist.github.com/lukeslp/2c97e17445d16d6515c85061c1aa78a0)

## Author

Luke Steuber | luke@lukesteuber.com | @lukesteuber.com (Bluesky)

## Structured Data (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Dataset",
  "name": "Strange Places v5.1 - Mysterious Phenomena",
  "description": "341,256 mysterious phenomena worldwide including UFO sightings, megaliths, caves, ghost towns, meteorites, fireballs, tornadoes, earthquakes, volcanoes, and shipwrecks from NASA, NOAA, USGS, OpenStreetMap, and the Megalithic Portal.",
  "url": "https://www.kaggle.com/datasets/lucassteuber/strange-places-mysterious-phenomena",
  "sameAs": "https://huggingface.co/datasets/lukeslp/strange-places",
  "license": "https://creativecommons.org/licenses/by/4.0/",
  "creator": {
    "@type": "Person",
    "name": "Luke Steuber",
    "url": "https://lukesteuber.com"
  },
  "keywords": ["UFO", "caves", "megaliths", "ghost towns", "meteorites", "earthquakes", "volcanoes", "tornadoes", "geospatial", "mysterious phenomena"],
  "temporalCoverage": "1950/2025",
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
