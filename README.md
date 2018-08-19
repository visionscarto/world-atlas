## Natural Earth vector data, fixed & packaged

### 110m:

- fixes topological issues on the border of Sudan
- adds a few Kuril Islands
- adds Gaza
- fixes id="578" for Norway
- countries with no official iso_n3 code receive a negative id

### 110m & 50m:

- uses UN definition for Morocco / Western Sahara
- export countries and land as GeoJSON
- publishes id in the tsv file


## Usage

You can use this as a drop-in replacement for [world-atlas](https://github.com/topojson/world-atlas) 110m and 50m data:

In TopoJSON:
```{javascript}
fetch('https://unpkg.com/visionscarto-world-atlas/world/110m.json').then(d => d.json())
```

In GeoJSON:
```{javascript}
fetch('https://unpkg.com/visionscarto-world-atlas/world/50m_land.geojson').then(d => d.json())
```

With d3:
```{javascript}
d3.json('https://unpkg.com/visionscarto-world-atlas/world/110m_countries.geojson')
```

…

## Credits

The hard work has been done by the team
at [Natural Earth](https://www.naturalearthdata.com/).

Mike Bostock has contributed all the necessary tooling
and examples in [world-atlas](https://github.com/topojson/world-atlas).
