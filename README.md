---
license: other
license_name: mixed-licenses
license_link: https://github.com/lukesteuber/strange-places-dataset/blob/main/LICENSE.md
task_categories:
  - other
language:
  - en
tags:
  - geography
  - earth-science
  - geospatial
  - natural-disasters
  - archaeology
  - caves
  - meteorites
  - ufo-sightings
  - tornadoes
  - earthquakes
  - volcanoes
  - megalithic-sites
  - ghost-towns
  - nasa
  - noaa
  - usgs
  - openstreetmap
  - real-world-data
  - coordinates
  - phenomena
size_categories:
  - 100K<n<1M
pretty_name: Strange Places v5.1 - Real-World Mysterious Phenomena
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
    - name: type
      dtype: string
    - name: magnitude
      dtype: float64
  splits:
    - name: train
      num_bytes: 151607296
      num_examples: 341256
  download_size: 151607296
  dataset_size: 151607296
configs:
  - config_name: default
    data_files:
      - split: train
        path: all_phenomena_unified_v5.1_no_waterfalls.json
---

# Strange Places v5.1: Real-World Mysterious Phenomena

<div align="center">
  <img src="https://img.shields.io/badge/records-341%2C256-blue" alt="Records">
  <img src="https://img.shields.io/badge/categories-12-green" alt="Categories">
  <img src="https://img.shields.io/badge/coordinates-99.9%25%20valid-brightgreen" alt="Coordinates">
  <img src="https://img.shields.io/badge/balance-EXCELLENT-success" alt="Balance">
  <img src="https://img.shields.io/badge/data-100%25%20real-orange" alt="Real Data">
</div>

## What's New in v5.1

**Waterfalls removed** - Not thematically consistent with "mysterious phenomena". Available as separate dataset: [Waterfalls Worldwide](https://huggingface.co/datasets/lukesteuber/waterfalls-worldwide) (80K+ records)

## About

**341,256 mysterious phenomena** from NASA, NOAA, USGS, OpenStreetMap, and the Megalithic Portal. Caves, ancient megaliths, UFO sightings, meteorite landings, tornadoes, ghost towns—12 categories, perfectly balanced (no single category exceeds 21%).

**Key Features:**
- 🌍 **Global Coverage**: 99.9% valid coordinates across all continents
- ⚖️ **Perfect Balance**: Largest category only 21%
- ✅ **100% Real Data**: NASA, NOAA, USGS, OpenStreetMap, Megalithic Portal
- 📊 **Rich Metadata**: 341,256 georeferenced records with timestamps, magnitudes, descriptions
- 🆕 **Fresh Data**: Version 5.1 released 2026-01-19

## Dataset Structure

### Data Fields

**Universal fields** (all records):
- `category`: Category name (string)
- `latitude`: Decimal degrees, -90 to 90 (float)
- `longitude`: Decimal degrees, -180 to 180 (float)

**Common optional fields**:
- `name`: Phenomenon name (string)
- `description`: Details and context (string)
- `date`: ISO 8601 date/timestamp (string)
- `type`: Subtype classification (string)
- `magnitude`: Intensity/size measure (float)
- Additional category-specific fields

### Data Splits

| Split | Examples |
|-------|----------|
| train | 341,256 |

### Categories

| Category | Count | % | Description |
|----------|-------|---|-------------|
| noaa_tornadoes | 71,813 | 21.0% | US tornado tracks 1950-2024 |
| osm_caves | 70,242 | 20.6% | Worldwide caves & formations |
| ufo_sightings | 60,632 | 17.8% | UFO reports 1910-2014 |
| megalithic_portal | 60,028 | 17.6% | Ancient stone monuments |
| nasa_meteorites | 32,186 | 9.4% | Meteorite landings |
| osm_ghost_towns | 18,154 | 5.3% | Abandoned settlements |
| noaa_storm_events | 14,770 | 4.3% | Significant weather events |
| noaa_thermal_springs | 5,003 | 1.5% | Hot springs |
| usgs_earthquakes | 3,742 | 1.1% | Seismic events 2016-2024 |
| noaa_shipwrecks | 3,653 | 1.1% | Historic shipwrecks |
| nasa_fireballs | 863 | 0.3% | Bright meteor observations |
| usgs_volcanoes | 170 | <0.1% | Active/dormant volcanoes |

## Dataset Creation

### Source Data

#### Data Collection

All data sourced from verified public repositories:

| Source | License | Records | Description |
|--------|---------|---------|-------------|
| NASA Open Data | Public Domain | 33,049 | Meteorites, fireballs |
| NOAA NCEI | Public Domain | 95,056 | Weather, climate events |
| USGS | Public Domain | 3,912 | Geological features |
| OpenStreetMap | ODbL 1.0 | 88,396 | Caves, ghost towns |
| Megalithic Portal | Unrestricted | 60,028 | Archaeological sites |
| CORGIS/NUFORC | Public Data | 60,632 | UFO sighting reports |

#### Data Processing

1. **Download**: Fetched from APIs, bulk downloads, KMZ/KML parsing
2. **Standardization**: Unified JSON schema across all categories
3. **Validation**:
   - Coordinate bounds checking (-90/90, -180/180)
   - Removed invalid coordinates (0,0 "Null Island", out of bounds)
   - Date format normalization
4. **Filtering**: NOAA storms reduced from 1.23M → 14.8K significant events (98.8% reduction)
5. **Balance Analysis**: Verified no single category dominates

### Annotations

No manual annotations. All data comes directly from source databases with original metadata preserved.

## Considerations for Using the Data

### Applications

- **Education**: Earth science, archaeology, climate science curricula
- **Research**: Spatial patterns, temporal trends, cross-domain correlations
- **Visualization**: Interactive maps, geographic storytelling
- **Disaster analysis**: Severe weather pattern research

### Discussion of Biases

Known limitations:
- **Geographic bias**: Some categories USA-heavy (tornadoes, UFO sightings)
- **Temporal inconsistency**: Date ranges vary by category (ancient to 2026)
- **Reporting bias**: UFO sightings reflect reporting patterns, not necessarily phenomena distribution
- **Data quality variance**: Crowdsourced (OSM) vs government (NASA/NOAA/USGS) data have different accuracy levels

### Other Known Limitations

- **Temporal coverage**: Not all categories span same time periods
- **Coordinate precision**: Varies by source (typically 4-6 decimal places)
- **Missing data**: 226 records (0.1%) have missing/invalid coordinates
- **Language**: English-centric descriptions and place names

## Additional Information

### Dataset Curators

**Luke Steuber**
- Email: luke@lukesteuber.com
- Bluesky: @lukesteuber.com
- GitHub: https://github.com/lukesteuber

### Licensing Information

**Mixed licenses** - Attribution required for OpenStreetMap and Megalithic Portal:

```
This dataset includes:
- U.S. Government data (NASA, NOAA, USGS): Public Domain
- OpenStreetMap data: © OpenStreetMap contributors, ODbL 1.0
- Megalithic Portal data: Unrestricted download (attribution requested)
- CORGIS/NUFORC data: Public Data
```

### Citation Information

```bibtex
@dataset{steuber2026strange,
  title={Strange Places v5.1: Real-World Mysterious Phenomena},
  author={Steuber, Luke},
  year={2026},
  publisher={Hugging Face},
  url={https://huggingface.co/datasets/lukesteuber/strange-places},
  note={341,256 georeferenced records across 12 categories}
}
```

### Contributions

Contributions welcome! Please open an issue or pull request on the [GitHub repository](https://github.com/lukesteuber/strange-places-dataset).

## Related Datasets

- [Waterfalls Worldwide](https://huggingface.co/datasets/lukesteuber/waterfalls-worldwide) - 80K+ waterfalls (separated from this dataset in v5.1)

## Example Usage

### Load Dataset

```python
from datasets import load_dataset

# Load full dataset
dataset = load_dataset("lukesteuber/strange-places")

# Access as pandas DataFrame
df = dataset['train'].to_pandas()
print(f"Total records: {len(df):,}")
print(df['category'].value_counts())
```

### Filter by Category

```python
# Get all caves
caves = dataset['train'].filter(lambda x: x['category'] == 'osm_caves')
print(f"Caves: {len(caves):,}")

# Get UFO sightings in California
ca_ufos = dataset['train'].filter(
    lambda x: x['category'] == 'ufo_sightings'
    and 32 <= x['latitude'] <= 42
    and -125 <= x['longitude'] <= -114
)
```

### Visualize on Map

```python
import folium
from folium.plugins import HeatMap

# Create heatmap of meteorite landings
meteorites = dataset['train'].filter(lambda x: x['category'] == 'nasa_meteorites')
heat_data = [[r['latitude'], r['longitude']] for r in meteorites]

m = folium.Map([20, 0], zoom_start=2)
HeatMap(heat_data).add_to(m)
m.save('meteorites_heatmap.html')
```

## Version History

- **v5.1** (2026-01-19): Waterfalls removed (available separately), 12 categories, 341K records
- **v5.0-balanced** (2026-01-19): +4 categories, +163K records, perfect balance
- **v4.0** (2026-01-XX): Initial release, 9 categories, 258K records

## Changelog

See [V5_RELEASE_NOTES.md](V5_RELEASE_NOTES.md) for detailed version history.
