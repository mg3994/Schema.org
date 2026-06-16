# Advanced Offers & E-commerce

Documentation for complex pricing models, shipping details, and inventory availability.

## Core Properties

*   **priceSpecification**: For complex pricing (e.g., membership price vs. regular price).
*   **shippingDetails**: Comprehensive shipping info.
*   **hasMerchantReturnPolicy**: Linking to return policies.
*   **eligibleQuantity**: For bulk pricing.
*   **validFrom / validThrough**: For sales and promotions.

---

## Comprehensive Example: Bulk Pricing & Shipping (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Organic Cotton T-Shirt",
  "offers": {
    "@type": "Offer",
    "price": "19.99",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock",
    "shippingDetails": {
      "@type": "OfferShippingDetails",
      "shippingRate": {
        "@type": "MonetaryAmount",
        "value": "5.00",
        "currency": "USD"
      },
      "deliveryTime": {
        "@type": "ShippingDeliveryTime",
        "handlingTime": {
          "@type": "QuantitativeValue",
          "value": "1",
          "unitCode": "DAY"
        },
        "transitTime": {
          "@type": "QuantitativeValue",
          "minValue": "2",
          "maxValue": "5",
          "unitCode": "DAY"
        }
      }
    },
    "hasMerchantReturnPolicy": {
      "@type": "MerchantReturnPolicy",
      "applicableCountry": "US",
      "returnPolicyCategory": "https://schema.org/MerchantReturnFiniteReturnWindow",
      "merchantReturnDays": 30,
      "returnMethod": "https://schema.org/ReturnByMail",
      "returnFees": "https://schema.org/FreeReturn"
    }
  }
}
```

## Tips for Advanced Offers
*   **Shipping Details**: In 2024-2025, Google increasingly uses `shippingDetails` to show shipping costs and delivery times directly in search results.
*   **Return Policy**: Use `hasMerchantReturnPolicy` to improve trust and click-through rates.
*   **Sales**: Use `validFrom` and `validThrough` to automate the start and end of promotional pricing in search results.

## Things to Avoid
*   **Hidden Fees**: Ensure the price marked up is the actual price the user will pay (excluding taxes/shipping if specified).
*   **Outdated Availability**: If a product goes out of stock, update the schema immediately to avoid frustrating users.
