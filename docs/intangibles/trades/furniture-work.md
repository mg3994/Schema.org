# Furniture Work & Services

Documentation for professionals specializing in furniture making, assembly, repair, and restoration.

## Core Types

*   **FurnitureStore**: For retail entities (already covered in [Retail Stores](../organizations/stores.md)).
*   **Service**: Specific tasks like "Custom Furniture Build", "Furniture Assembly", "Upholstery Repair".
*   **LocalBusiness**: General type for furniture service companies.

---

## Comprehensive Example: Custom Furniture Maker & Repair (JSON-LD)

This example covers a professional who builds custom pieces and also offers restoration services.

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "The Furniture Artisan",
  "description": "Bespoke furniture creation and antique restoration services.",
  "image": "https://example.com/furniture-workshop.jpg",
  "telephone": "+15554443333",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Furniture Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Bespoke Dining Table",
          "description": "Custom designed and handcrafted solid oak dining tables."
        },
        "priceSpecification": {
          "@type": "PriceSpecification",
          "minPrice": "1200.00",
          "priceCurrency": "USD"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Furniture Assembly",
          "description": "On-site assembly of flat-pack furniture."
        },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "50.00",
          "priceCurrency": "USD",
          "unitText": "hour"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Antique Restoration",
          "description": "Professional refinishing and structural repair of antique furniture."
        },
        "priceSpecification": {
          "@type": "PriceSpecification",
          "price": "250.00",
          "priceCurrency": "USD",
          "description": "Starting price for minor restoration."
        }
      }
    ]
  }
}
```

## Tips for Furniture Professionals
*   **Assembly Services**: For flat-pack assembly, use `UnitPriceSpecification` with an hourly rate or a flat rate per item.
*   **Materials**: Clearly state in the `description` if materials (fabrics for upholstery, specific wood types) are included in the price.
*   **Portfolio**: Use the `image` property within individual `Service` items to show examples of past furniture work.
*   **Customization**: Use `potentialAction` with `QuoteAction` to allow clients to request prices for specific designs.

## Things to Avoid
*   **Vague Pricing**: Furniture work varies greatly; always use `minPrice` or specify "starting from" in the description.
*   **Missing Lead Times**: Hand-made furniture takes time; mention estimated completion times in the offer description.
