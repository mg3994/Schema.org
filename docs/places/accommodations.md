# Accommodations Schema Documentation

Documentation for places where users can stay, such as hotels, apartments, and vacation rentals.

## Core Types

*   **Hotel**: A standard hotel.
*   **BedAndBreakfast**: A B&B.
*   **Hostel**: A hostel.
*   **Motel**: A motel.
*   **Resort**: A resort.
*   **Apartment**: A single apartment for rent.
*   **VacationRental**: A short-term rental property.
*   **House**: A single family home.

---

## Comprehensive Example: Hotel with Room Details (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Hotel",
  "name": "The Grand Azure",
  "starRating": {
    "@type": "Rating",
    "ratingValue": "5"
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "777 Seaside Way",
    "addressLocality": "Miami",
    "addressRegion": "FL"
  },
  "amenityFeature": [
    { "@type": "LocationFeatureSpecification", "name": "Free Wi-Fi", "value": "true" },
    { "@type": "LocationFeatureSpecification", "name": "Pool", "value": "true" }
  ],
  "containsPlace": [
    {
      "@type": "HotelRoom",
      "name": "Ocean View Suite",
      "bed": {
        "@type": "BedDetails",
        "numberOfBeds": 1,
        "typeOfBed": "King"
      },
      "occupancy": {
        "@type": "QuantitativeValue",
        "value": 2
      }
    }
  ]
}
```

## Tips for Accommodations
*   **Star Rating**: Always include the official `starRating` if available.
*   **Amenities**: Be exhaustive with `amenityFeature`.
*   **Rooms**: Use `containsPlace` with `HotelRoom` to describe specific room types.
*   **Occupancy**: Specify the max `occupancy` for each room.

## Things to Avoid
*   **Vague Bed Info**: Use the `BedDetails` object for clarity.
*   **Mismatched Ratings**: Ensure the `starRating` is the official one, not just a user review average.
