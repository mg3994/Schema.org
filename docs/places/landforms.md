# Landforms & Geographic Features

Documentation for describing natural geographic features like mountains, bodies of water, and continents.

## Core Types

*   **Landform**: The base type for all natural features.
*   **Mountain**: A large natural elevation of the earth's surface.
*   **Volcano**: A mountain or hill having a crater or vent through which lava, rock fragments, hot vapor, and gas are being or have been erupted from the earth's crust.
*   **Continent**: One of the world's main continuous expanses of land.
*   **BodyOfWater**: A significant accumulation of water.
    *   **OceanBodyOfWater**: A very large expanse of sea.
    *   **SeaBodyOfWater**: A large body of salt water.
    *   **RiverBodyOfWater**: A large natural stream of water flowing in a channel to the sea, a lake, or another such stream.
    *   **LakeBodyOfWater**: A large body of water surrounded by land.
    *   **Waterfall**: A cascade of water falling from a height.
    *   **Canal**: An artificial waterway.

---

## Comprehensive Example: Mountain (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Mountain",
  "name": "Mount Everest",
  "description": "The highest mountain above sea level, located in the Mahalangur Himal sub-range of the Himalayas.",
  "image": "https://example.com/photos/everest.jpg",
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "27.9881",
    "longitude": "86.9250"
  },
  "elevation": {
    "@type": "QuantitativeValue",
    "value": "8848.86",
    "unitCode": "MTR"
  },
  "containedInPlace": {
    "@type": "Continent",
    "name": "Asia"
  }
}
```

## Comprehensive Example: River (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "RiverBodyOfWater",
  "name": "Amazon River",
  "description": "The largest river by discharge volume of water in the world.",
  "geo": {
    "@type": "GeoShape",
    "line": "..."
  },
  "containedInPlace": [
    { "@type": "Country", "name": "Brazil" },
    { "@type": "Country", "name": "Peru" },
    { "@type": "Country", "name": "Colombia" }
  ]
}
```

## Tips for Landforms
*   **Elevation**: Use `elevation` with `QuantitativeValue` and `unitCode: MTR` (Meters) or `FOT` (Feet).
*   **Geo Shapes**: For large features like rivers or mountain ranges, use `GeoShape` with `line` or `polygon` to describe the extent.
*   **Parent Places**: Use `containedInPlace` to link to the `Continent` or `Country`.

## Things to Avoid
*   **Missing Coordinates**: Even for massive features, a central `GeoCoordinates` point is helpful for search engines.
*   **Confusing with TouristAttraction**: While a mountain might be a tourist attraction, use the most specific type (`Mountain`) as the primary type.
