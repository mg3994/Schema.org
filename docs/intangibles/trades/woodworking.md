# Woodworking, Carpentry & Furniture Makers

Documentation for woodworkers, carpenters, and artisans who work with wood.

## Core Types

*   **LocalBusiness / HomeAndConstructionBusiness**: General business type.
*   **Occupation**: Use `Carpenter` in the occupation name.
*   **ProductGroup**: For custom furniture lines.
*   **Service**: Specific tasks like "Cabinet Making" or "Deck Repair".

---

## Comprehensive Example: Custom Furniture Maker (JSON-LD)

This example shows a woodworker who makes custom items (ProductGroup) and provides repair services.

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Artisan Oak Woodworking",
  "description": "Custom handmade furniture and architectural woodworking.",
  "telephone": "+15552224444",
  "knowsAbout": ["Cabinetry", "Hardwood Restoration", "Custom Joinery"],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Woodworking Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Furniture Repair & Refinishing",
          "description": "Restoring antique or damaged wood furniture."
        },
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "85.00",
          "priceCurrency": "USD",
          "unitText": "hour"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Custom Cabinet Design",
          "description": "Full design and build for kitchen or office cabinets."
        },
        "priceSpecification": {
          "@type": "PriceSpecification",
          "minPrice": "2500.00",
          "priceCurrency": "USD",
          "description": "Minimum project price."
        }
      }
    ]
  }
}
```

## Tips for Woodworkers
*   **Materials vs. Labor**: Use the `description` in the `Offer` to clarify if high-quality hardwoods (like Walnut or Oak) are included or extra.
*   **Portfolio**: Use the `image` property to link to photos of completed projects.
*   **Custom Orders**: Use `potentialAction` with `QuoteAction` to allow users to request pricing for custom designs.
*   **Sustainability**: Use the `description` or `award` properties to mention if you use reclaimed wood or sustainable practices.

## Things to Avoid
*   **Vague Wood Types**: If you specialize in specific woods, mention them.
*   **Missing Lead Times**: Woodworking takes time; mentioning approximate "lead times" in the description is helpful for users.
*   **No Physical Address**: Even if you work from a home workshop, providing an `addressLocality` is important for local search.
