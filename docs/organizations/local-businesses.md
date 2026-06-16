# Local Business Schema Documentation

A `LocalBusiness` is a particular physical business or branch of an organization. Examples include restaurants, banks, pet stores, etc.

## Major Sub-types

The hierarchy is deep. Here are the main branches:
*   **AutomotiveBusiness**: Auto dealers, repair shops.
*   **EmergencyService**: Fire stations, hospitals, police.
*   **EntertainmentBusiness**: Art galleries, casinos, movie theaters.
*   **FinancialService**: Banks, accounting services.
*   **FoodEstablishment**: Restaurants, cafes, bars, bakeries.
*   **GovernmentOffice**: Post offices.
*   **HealthAndBeautyBusiness**: Beauty salons, gyms, spas.
*   **HomeAndConstructionBusiness**: Electricians, plumbers, painters.
*   **LegalService**: Attorneys, notaries.
*   **LodgingBusiness**: Hotels, motels, hostels, bed and breakfasts.
*   **MedicalBusiness**: Clinics, pharmacies, physicians.
*   **ProfessionalService**: General professional services.
*   **RealEstateAgent**: Real estate agencies.
*   **ShoppingCenter**: Malls and centers.
*   **SportsActivityLocation**: Golf courses, gyms, stadiums.
*   **Store**: Clothing stores, grocery stores, electronics stores.

---

## Comprehensive Example: Restaurant (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Restaurant",
  "name": "The Golden Fork",
  "image": "https://example.com/photos/restaurant.jpg",
  "@id": "https://example.com/#restaurant",
  "url": "https://example.com",
  "telephone": "+15551234567",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "456 Culinary Ave",
    "addressLocality": "New York",
    "addressRegion": "NY",
    "postalCode": "10001",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 40.7128,
    "longitude": -74.0060
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "11:00",
      "closes": "22:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Saturday", "Sunday"],
      "opens": "10:00",
      "closes": "23:00"
    }
  ],
  "menu": "https://example.com/menu",
  "servesCuisine": "Modern Italian",
  "priceRange": "$$$",
  "acceptsReservations": "true",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "245"
  }
}
```

## Tips for Local Businesses
*   **Specific Types**: Don't just use `LocalBusiness`. Use `Dentist`, `Bakery`, or `Hotel`. Specificity helps Google categorize you.
*   **Opening Hours**: Use `openingHoursSpecification` for complex hours, including holiday hours.
*   **Price Range**: Use `$`, `$$`, `$$$`, or `$$$$` to help users understand your price point.
*   **Coordinates**: Provide `geo` (latitude and longitude). This is vital for appearing in map-based searches.
*   **Department**: If a business has multiple departments (e.g., a pharmacy inside a grocery store), use the `department` property to link them.

## Things to Avoid
*   **Inconsistent NAP**: We'll say it again: Name, Address, and Phone must be consistent everywhere.
*   **Review Spam**: Only include `aggregateRating` if the reviews are actually visible on your page and can be verified.
*   **Outdated Hours**: Keep your hours updated, especially for holidays.
