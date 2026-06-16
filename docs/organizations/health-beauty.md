# Health & Beauty Business Schema

Documentation for salons, spas, gyms, and other health and beauty-related local businesses.

## Core Types

*   **BeautySalon**: For hair, nails, and general beauty services.
*   **DaySpa**: For spa and relaxation services.
*   **HairSalon**: Specifically for hair services.
*   **HealthClub / ExerciseGym**: For fitness and workout facilities.
*   **TattooParlor**: For tattoo and piercing services.
*   **NailSalon**: Specifically for nail services.

---

## Comprehensive Example: Day Spa with Services (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "DaySpa",
  "name": "Serenity Wellness Spa",
  "image": "https://example.com/spa.jpg",
  "priceRange": "$$$",
  "telephone": "+15559876543",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "456 Relaxation Lane",
    "addressLocality": "Zen City",
    "addressRegion": "CA",
    "postalCode": "90210"
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"],
      "opens": "09:00",
      "closes": "20:00"
    }
  ],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Spa Treatments",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Swedish Massage",
          "description": "A relaxing 60-minute full body massage."
        },
        "price": "90.00",
        "priceCurrency": "USD"
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Facial Treatment",
          "description": "Deep cleansing and hydration for all skin types."
        },
        "price": "75.00",
        "priceCurrency": "USD"
      }
    ]
  }
}
```

## Tips for Health & Beauty
*   **Offer Catalogs**: These businesses often have a wide variety of services. Use `OfferCatalog` to organize them into groups (e.g., "Massage", "Facials", "Memberships").
*   **Opening Hours**: Be precise, especially if hours vary by day or if you are closed on specific days like Monday.
*   **Price Range**: Use `$` signs to give users an immediate idea of the cost level.
*   **Appointments**: Use `potentialAction` with `ReserveAction` to link to your booking system.

## Things to Avoid
*   **Generic Images**: Use actual photos of your facility or staff to build trust.
*   **Outdated Prices**: Ensure the prices in your catalog match your current menu.
*   **Missing Phone Number**: Local beauty businesses are highly dependent on phone bookings; don't forget the `telephone` property.
