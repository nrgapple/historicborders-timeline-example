# Historic Country Borders Example

This is an example of historic borders data taken from [aourednik's country borders repo](https://github.com/aourednik/historical-basemaps).

## Create and visualize your own timeline data

1. Create a new github repo. **Make sure to name your repo `historicborders-[timeline-name]`**
2. Follow the schema from this repo.
3. Visit `https://historyborders.com/timeline/[your-github-username]/[timeline-name]`

### Folder structure

```
years
|
+- [year].geojson
|
+- bc[year].geojson

config.json
```

### Config file `config.json`

```json
{
  "name": "Your timeline name here",
  "description": "A short description"
}
```

### Years geojson

Your geojson should be all the borders for countries in a given year. They must be a `FeatureCollection` of `multipolygons`.

#### Example

```json
// 1700
{
  "type": "FeatureCollection",
  "name": "world_1700",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "NAME": "Country Name"
      },
      "geometry": {
        "type": "MultiPolygon",
        "coordinates": [[]]
      }
    }
  ]
}
```
