# Specialized Retail Stores

Documentation for various types of physical and online retail stores.

## Core Types

*   **Store**: The base type for all retail stores.
*   **BookStore**: A shop selling books.
*   **ClothingStore**: A shop selling clothes and fashion.
*   **ElectronicsStore**: A shop selling electronic goods.
*   **GroceryStore / Supermarket**: A shop selling food and household goods.
*   **HardwareStore**: A shop selling tools and building materials.
*   **JewelryStore**: A shop selling jewelry and watches.
*   **LiquorStore**: A shop selling alcoholic beverages.
*   **PetStore**: A shop selling pets and pet supplies.
*   **ShoeStore**: A shop selling footwear.
*   **ToyStore**: A shop selling toys and games.
*   **WholesaleStore**: A shop selling goods in large quantities.

---

## Comprehensive Example: Clothing Store with Inventory (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ClothingStore",
  "name": "Urban Threads",
  "image": "https://example.com/storefront.jpg",
  "priceRange": "$$",
  "telephone": "+15551234567",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Fashion Ave",
    "addressLocality": "New York",
    "addressRegion": "NY",
    "postalCode": "10001"
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "10:00",
      "closes": "20:00"
    }
  ],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Seasonal Collection",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Product",
          "name": "Organic Cotton Tee",
          "brand": "EcoWear"
        },
        "price": "25.00",
        "priceCurrency": "USD"
      }
    ]
  }
}
```

## Tips for Retail Stores
*   **Specific Types**: Always use the most specific store type (e.g., `BikeStore` instead of just `Store`).
*   **Department**: If a store has multiple departments, use the `department` property to link them.
*   **Inventory**: Use `hasOfferCatalog` or `makesOffer` to link to your products.
*   **Payment Methods**: Specify accepted payment methods using `paymentAccepted`.

## Things to Avoid
*   **Missing Prices**: Use `priceRange` to give users an idea of the cost.
*   **Generic Descriptions**: Be specific about the brands or types of products you carry.
*   **Broken Storefront Images**: A high-quality image of the physical store is vital for local SEO.
