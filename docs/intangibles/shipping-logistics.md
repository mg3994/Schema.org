# Shipping & Logistics

Documentation for describing shipping costs, delivery times, and logistics for e-commerce.

## Core Types

*   **OfferShippingDetails**: Comprehensive container for shipping info.
*   **ShippingDeliveryTime**: Details on handling and transit time.
*   **ShippingRateSettings**: Information about shipping rates and areas served.
*   **DeliveryMethod**: The method of delivery (Locker, Parcel, etc.).
*   **DefinedRegion**: The geographic region where the shipping policy applies.

---

## Comprehensive Example: Complex Shipping Policy (JSON-LD)

This example shows free shipping for a specific region with detailed delivery times.

```json
{
  "@context": "https://schema.org",
  "@type": "OfferShippingDetails",
  "shippingRate": {
    "@type": "MonetaryAmount",
    "value": "0.00",
    "currency": "USD"
  },
  "shippingDestination": {
    "@type": "DefinedRegion",
    "addressCountry": "US",
    "addressRegion": ["CA", "OR", "WA"]
  },
  "deliveryTime": {
    "@type": "ShippingDeliveryTime",
    "handlingTime": {
      "@type": "QuantitativeValue",
      "minValue": 0,
      "maxValue": 1,
      "unitCode": "DAY"
    },
    "transitTime": {
      "@type": "QuantitativeValue",
      "minValue": 2,
      "maxValue": 3,
      "unitCode": "DAY"
    },
    "cutoffTime": "14:00:00Z",
    "businessDays": {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]
    }
  }
}
```

## Tips for Logistics
*   **Cutoff Time**: Use `cutoffTime` to help search engines display "Order within X hours for delivery by Y".
*   **Business Days**: Explicitly define `businessDays` so transit calculations are accurate.
*   **Region Specifics**: Use `DefinedRegion` to create different shipping objects for different states or countries.
*   **Weight-Based Shipping**: Combine with `shippingWeight` on the `Product` for precision.

## Things to Avoid
*   **Vague Ranges**: Use `minValue` and `maxValue` for transit times instead of just a string.
*   **Missing Currency**: Always include `priceCurrency` or `currency` in monetary amounts.
*   **Inconsistent Data**: Ensure your marked-up shipping costs match your checkout page exactly.
