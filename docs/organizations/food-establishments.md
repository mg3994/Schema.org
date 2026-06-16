# Food Establishments & Menus

Documentation for restaurants, cafes, and bars, including detailed menu structures.

## Core Types

*   **Restaurant**: A food establishment.
*   **Menu**: A list of food and drinks.
*   **MenuSection**: A category within a menu (e.g., "Appetizers", "Main Course").
*   **MenuItem**: A specific dish or drink.

---

## Comprehensive Example: Restaurant with Menu (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Restaurant",
  "name": "The Gourmet Bistro",
  "image": "https://example.com/bistro.jpg",
  "telephone": "+15551234567",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "789 Culinary Lane",
    "addressLocality": "Foodie Town"
  },
  "hasMenu": {
    "@type": "Menu",
    "name": "Dinner Menu",
    "mainEntityOfPage": "https://example.com/menu",
    "hasMenuSection": [
      {
        "@type": "MenuSection",
        "name": "Starters",
        "hasMenuItem": [
          {
            "@type": "MenuItem",
            "name": "Truffle Fries",
            "description": "Crispy fries with truffle oil and parmesan.",
            "offers": {
              "@type": "Offer",
              "price": "12.00",
              "priceCurrency": "USD"
            }
          }
        ]
      },
      {
        "@type": "MenuSection",
        "name": "Main Courses",
        "hasMenuItem": [
          {
            "@type": "MenuItem",
            "name": "Pan-Seared Salmon",
            "description": "Wild-caught salmon with lemon butter sauce.",
            "offers": {
              "@type": "Offer",
              "price": "28.00",
              "priceCurrency": "USD"
            },
            "suitableForDiet": "https://schema.org/GlutenFreeDiet"
          }
        ]
      }
    ]
  }
}
```

## Tips for Food Establishments
*   **Dietary Restrictions**: Use `suitableForDiet` (e.g., `GlutenFreeDiet`, `VeganDiet`) on `MenuItem` to help users with dietary needs.
*   **Cuisine**: Specify `servesCuisine` (e.g., "Italian", "Fusion").
*   **Reservations**: Link to your booking system using `acceptsReservations` and `potentialAction`.
*   **Delivery**: Use `OrderAction` to show that you offer online ordering.

## Things to Avoid
*   **Outdated Menus**: Ensure prices and items match your current in-store offerings.
*   **Missing Prices**: Search results often highlight prices; ensure every `MenuItem` has an `Offer`.
*   **Generic Images**: Use high-quality photos of your actual dishes.
