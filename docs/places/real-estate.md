# Real Estate Schema Documentation

Documentation for property listings, apartment complexes, and floor plans.

## Core Types

*   **RealEstateListing**: An individual listing for a property.
*   **ApartmentComplex**: A complex of apartments.
*   **SingleFamilyResidence**: A standalone house.
*   **GatedResidenceCommunity**: A gated community.
*   **FloorPlan**: The layout of a specific unit or building.

---

## Comprehensive Example: RealEstateListing with FloorPlan (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "RealEstateListing",
  "name": "Luxury Penthouse in Downtown",
  "datePosted": "2025-04-01",
  "description": "Stunning 3-bedroom penthouse with panoramic city views.",
  "offers": {
    "@type": "Offer",
    "price": "2500000.00",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock"
  },
  "mainEntity": {
    "@type": "Apartment",
    "name": "Unit 50A",
    "numberOfRooms": 5,
    "floorSize": {
      "@type": "QuantitativeValue",
      "value": "2500",
      "unitCode": "FTK"
    },
    "accommodationCategory": "Penthouse",
    "amenityFeature": [
      { "@type": "LocationFeatureSpecification", "name": "Private Balcony", "value": true },
      { "@type": "LocationFeatureSpecification", "name": "Smart Home System", "value": true }
    ],
    "layoutImage": {
      "@type": "ImageObject",
      "url": "https://example.com/floorplans/unit-50a.png"
    }
  }
}
```

## Tips for Real Estate
*   **Floor Size**: Always include the `floorSize` using `QuantitativeValue`. Common unit codes are `FTK` for square feet and `MTK` for square meters.
*   **Images**: High-quality interior and exterior images are essential.
*   **Amenities**: List all major amenities like "Pool", "Gym", "Garage", etc.
*   **Status**: Keep the listing status updated (e.g., Sold, Pending, Available).

## Things to Avoid
*   **Inaccurate Prices**: Ensure the `price` in the schema matches the advertised price.
*   **Missing Addresses**: A listing must have a precise `PostalAddress`.
*   **Low-Res Floor Plans**: Users and search engines need clear, readable layout images.
