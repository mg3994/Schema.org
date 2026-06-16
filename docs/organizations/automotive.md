# Automotive Businesses

Documentation for car dealerships, repair shops, and vehicle services.

## Core Types

*   **AutoDealer**: A business that sells vehicles.
*   **AutoRepair**: A shop that repairs vehicles.
*   **AutoBodyShop**: A shop that performs body work.
*   **AutoRental**: A business that rents vehicles.
*   **GasStation**: A station providing fuel.

---

## Comprehensive Example: Auto Dealer with Inventory (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "AutoDealer",
  "name": "Elite Motors",
  "url": "https://www.elitemotors.com",
  "telephone": "+15550002222",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "100 Speed Way",
    "addressLocality": "Auto City"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Current Inventory",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Car",
          "name": "2024 Volt Sedan",
          "brand": "VoltMotors",
          "fuelType": "Electric"
        },
        "price": "45000.00",
        "priceCurrency": "USD"
      }
    ]
  }
}
```

## Tips for Auto Businesses
*   **Inventory**: Link your dealership to a catalog of `Vehicle` types (`Car`, `Motorcycle`).
*   **Specialties**: For repair shops, use `knowsAbout` or `description` to specify brands you specialize in.
*   **Opening Hours**: Use `openingHoursSpecification` for service vs. sales hours.
*   **Brand**: Link to the brands you represent using the `brand` property.

## Things to Avoid
*   **Missing VIN**: For specific used vehicles, the `vin` is the most important identifier.
*   **Vague Service Offerings**: Clearly list services like "Oil Change", "Brake Repair", etc.
