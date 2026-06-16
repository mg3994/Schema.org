# Places Schema Documentation

A `Place` represents entities that have a somewhat fixed, physical extension.

## Major Sub-types

*   **Accommodation**: Places to stay (Apartments, Houses, Hotels).
*   **AdministrativeArea**: Cities, Countries, States.
*   **CivicStructure**: Airports, Museums, Parks, Stadiums.
*   **Landform**: Mountains, Oceans, Rivers, Volcanoes.
*   **LandmarksOrHistoricalBuildings**: Significant landmarks.
*   **LocalBusiness**: (Also covered under Organizations) Physical businesses.
*   **Residence**: Apartment complexes, Gated communities.
*   **TouristAttraction**: Places that attract tourists.

## Comprehensive List of Types

*   **Apartment**: A single apartment.
*   **CampingPitch**: A spot for camping.
*   **House**: A single house.
*   **Room**: A room (Hotel room, Meeting room).
*   **City / Country / State**: Administrative regions.
*   **Airport / BusStation / SubwayStation**: Transit hubs.
*   **Museum / Park / Zoo**: Public places.
*   **Cemetery / Crematorium**: Funerary places.
*   **PlaceOfWorship**: Churches, Mosques, Synagogues.
*   **BodyOfWater**: Lakes, Oceans, Rivers.
*   **Continent**: Continents.

---

## Comprehensive Example: TouristAttraction (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TouristAttraction",
  "name": "Eiffel Tower",
  "description": "The Eiffel Tower is a wrought-iron lattice tower on the Champ de Mars in Paris, France.",
  "image": "https://example.com/eiffel.jpg",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Champ de Mars, 5 Avenue Anatole France",
    "addressLocality": "Paris",
    "postalCode": "75007",
    "addressCountry": "FR"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 48.8584,
    "longitude": 2.2945
  },
  "url": "https://www.toureiffel.paris/en",
  "telephone": "+33 892 70 12 39",
  "publicAccess": "true",
  "isAccessibleForFree": "false",
  "amenityFeature": [
    {
      "@type": "LocationFeatureSpecification",
      "name": "Elevator",
      "value": "true"
    },
    {
      "@type": "LocationFeatureSpecification",
      "name": "Restaurant",
      "value": "true"
    }
  ]
}
```

## Tips for Places
*   **Geo-Coding**: Always include `geo` coordinates for precise mapping.
*   **Accessibility**: Use properties like `publicAccess` and `isAccessibleForFree` to provide useful user info.
*   **Amenity Features**: Use `amenityFeature` to list specific features of a place like Wi-Fi, elevators, or parking.
*   **Parent Place**: Use `containedInPlace` to show hierarchy (e.g., a specific shop inside a mall).

## Things to Avoid
*   **Vague Addresses**: Don't just provide a city; provide a full `streetAddress` whenever possible.
*   **Confusing Types**: Don't use `Place` if the entity is primarily a `LocalBusiness`. Use the business type instead.
*   **Old Data**: If a place is permanently closed, use the `SpecialAnnouncement` or update its status.
