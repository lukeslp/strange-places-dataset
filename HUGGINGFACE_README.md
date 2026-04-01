---
license: cc-by-4.0
task_categories:
  - feature-extraction
language:
  - en
tags:
  - geography
  - ufos
  - meteorites
  - earthquakes
  - geospatial
  - phenomena
  - mapping
pretty_name: Strange Places v5.2
size_categories:
  - 100K<n<1M
---

# Strange Places v5.2

354K georeferenced phenomena: UFOs, bigfoot, meteorites, earthquakes, caves

354,770 georeferenced mysterious phenomena from NASA, NOAA, USGS, BFRO, NUFORC, OpenStreetMap, the Megalithic Portal, and the Shadowlands Haunted Places Index. Every record comes from authoritative databases -- no synthetic data.

Includes UFO sightings, bigfoot reports, meteorite landings, caves, megaliths, earthquakes, volcanoes, tornadoes, storms, shipwrecks, thermal springs, ghost towns, haunted places, and fireballs.

All real coordinates from government and authoritative sources. Global coverage.

## Dataset Structure

See `demo_notebook.ipynb` for data exploration examples.

## Usage

```python
from datasets import load_dataset

# Load the dataset
dataset = load_dataset("lukeslp/strange-places-mysterious-phenomena")

# Or load from local files
import json
with open('data.json') as f:
    data = json.load(f)
```

## Citation

```bibtex
@dataset{strange_places_mysterious_phenomena_2026,
  title = {Strange Places v5.2},
  author = {Steuber, Luke},
  year = {2026},
  url = {https://huggingface.co/datasets/lukeslp/strange-places-mysterious-phenomena}
}
```


## Distribution

- **Kaggle**: [lucassteuber/strange-places-mysterious-phenomena](https://www.kaggle.com/datasets/lucassteuber/strange-places-mysterious-phenomena)

## Author

**Luke Steuber**
- Website: [lukesteuber.com](https://lukesteuber.com)
- Bluesky: [@lukesteuber.com](https://bsky.app/profile/lukesteuber.com)
- Email: luke@lukesteuber.com

## License

CC-BY-4.0
