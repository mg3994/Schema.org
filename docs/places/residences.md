# Residences & Housing Communities

Documentation for describing large-scale residential entities like apartment complexes and gated communities.

## Core Types

*   **Residence**: The base for all housing.
*   **ApartmentComplex**: A building or group of buildings containing apartments.
*   **GatedResidenceCommunity**: A community with restricted access.
*   **SingleFamilyResidence**: A standalone house.

---

## Comprehensive Example: Apartment Complex (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ApartmentComplex",
  "name": "Skyline Heights Apartments",
  "description": "Modern luxury living in the heart of the city.",
  "image": "https://example.com/complex.jpg",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Skyline Drive",
    "addressLocality": "Metropolis",
    "addressRegion": "NY"
  },
  "telephone": "+15551234444",
  "numberOfAccommodationUnits": {
    "@type": "QuantitativeValue",
    "value": 250
  },
  "amenityFeature": [
    { "@type": "LocationFeatureSpecification", "name": "Rooftop Garden", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "24/7 Gym", "value": true }
  ],
  "petsAllowed": "Yes",
  "url": "https://www.skylineheights.com"
}
```

## Tips for Housing
*   **Capacity**: Use `numberOfAccommodationUnits` to show the size of the complex.
*   **Amenities**: List shared features (Pool, Gym, Parking) using `amenityFeature`.
*   **Pet Policy**: Use `petsAllowed` (Boolean or string) to clarify the policy.
*   **Units**: Link to specific `Apartment` types using `containsPlace`.

## Things to Avoid
*   **Vague Locations**: Ensure the `address` is precise.
*   **Generic Descriptions**: Detail what makes the community unique (e.g., "Near public transit", "Eco-friendly").
