# Sync Notes

## Locations

1. **~/datasets/strange-places-mysterious-phenomena/** (master)
   - Source: HuggingFace clone
   - File: `strange_places_v5.2.json` (354,770 records, 132MB)
   - Keep synced with HuggingFace

2. **~/html/datavis/data_trove/published/hf/strange-places-mysterious-phenomena/**
   - Purpose: Data trove catalog entry
   - Should have: README.md + full dataset file
   - Update when HuggingFace updates

3. **~/html/datavis/interactive/strange-places/data/phenomena.json**
   - Purpose: Optimized for web visualization
   - File: 27MB processed version
   - Manually updated as needed for viz

## When to Update

- HuggingFace updated → clone to ~/datasets/ → copy to data_trove
- Interactive viz needs refresh → process dataset → update phenomena.json
