# Civic Structures & Transit Hubs

Documentation for public and civic buildings, including transit stations, museums, and stadiums.

## Core Types

*   **Airport**: A place where aircraft take off and land.
*   **BusStation / BusStop**: Points for bus transit.
*   **SubwayStation / TrainStation**: Rail transit hubs.
*   **Museum**: A building for exhibiting art or history.
*   **StadiumOrArena**: For sports or large events.
*   **GovernmentBuilding**: City halls, courthouses, embassies.
*   **PlaceOfWorship**: Churches, mosques, synagogues.

---

## Comprehensive Example: Airport with Details (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Airport",
  "name": "San Francisco International Airport",
  "iataCode": "SFO",
  "icaoCode": "KSFO",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "SFO Airport",
    "addressLocality": "San Francisco",
    "addressRegion": "CA",
    "postalCode": "94128",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 37.6213,
    "longitude": -122.3790
  },
  "url": "https://www.flysfo.com/",
  "openingHours": "Mo-Su 00:00-23:59"
}
```

## Tips for Civic Structures
*   **IATA/ICAO Codes**: Essential for `Airport` identification.
*   **Transit Connections**: Use `containedInPlace` or `geo` to show physical relationships between stations.
*   **Opening Hours**: Most transit hubs are open 24/7, but museums and government buildings have strict hours.
*   **Amenities**: List features like "Free Wi-Fi" or "Parking" using `amenityFeature`.

## Things to Avoid
*   **Vague Naming**: Use the full official name of the building.
*   **Missing Geo Data**: Transit hubs are primary targets for map-based searches; always include `geo` coordinates.
