# Products Schema Documentation

A `Product` is anything that is made available for sale—for example, a pair of shoes, a concert ticket, or a car.

## Major Sub-types

*   **IndividualProduct**: A single, specific product.
*   **ProductGroup**: A group of products (e.g., a specific model of shirt in different colors).
*   **ProductModel**: A specific model of a product.
*   **Vehicle**: Buses, Cars, Motorcycles.
*   **DietarySupplement**: Supplements and vitamins.
*   **Drug**: Pharmaceutical products.

## Comprehensive List of Types

*   **BusOrCoach / Car / Motorcycle / MotorizedBicycle**: Types of vehicles.
*   **ProductCollection**: A collection of products.
*   **SomeProducts**: A collection of products that are not individually identified.

---

## Comprehensive Example: Product with Offers & Reviews (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Elite Wireless Headphones Z1",
  "image": [
    "https://example.com/photos/1x1/photo.jpg",
    "https://example.com/photos/4x3/photo.jpg"
  ],
  "description": "Professional-grade noise-canceling wireless headphones.",
  "sku": "99A12345",
  "mpn": "925872",
  "brand": {
    "@type": "Brand",
    "name": "AudioMax"
  },
  "review": {
    "@type": "Review",
    "reviewRating": {
      "@type": "Rating",
      "ratingValue": "4",
      "bestRating": "5"
    },
    "author": {
      "@type": "Person",
      "name": "John Doe"
    }
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.4",
    "reviewCount": "89"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://example.com/product/z1",
    "priceCurrency": "USD",
    "price": "199.99",
    "priceValidUntil": "2025-12-31",
    "itemCondition": "https://schema.org/NewCondition",
    "availability": "https://schema.org/InStock",
    "shippingDetails": {
      "@type": "OfferShippingDetails",
      "shippingRate": {
        "@type": "MonetaryAmount",
        "value": "0.00",
        "currency": "USD"
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
          "minValue": 1,
          "maxValue": 5,
          "unitCode": "DAY"
        }
      }
    }
  }
}
```

## Tips for Products
*   **Identifiers**: Always include `sku`, `gtin8`, `gtin12`, `gtin13`, or `mpn`. These are the most important fields for Google Shopping and Merchant Center.
*   **Price and Availability**: Use the `offers` property to define price, currency, and availability status (e.g., `InStock`, `OutOfStock`).
*   **Ratings**: `aggregateRating` is the key to getting those "Stars" in search results.
*   **Condition**: Explicitly state if the product is `NewCondition`, `UsedCondition`, or `RefurbishedCondition`.

## Things to Avoid
*   **Price in Description**: Don't put the price in the `description`. Use the `price` field in `offers`.
*   **Missing Currency**: Always include `priceCurrency`.
*   **Aggregated Ratings without Individual Reviews**: Google prefers when you have actual user reviews to back up the aggregate rating.
*   **Inaccurate Availability**: If a product is out of stock, your schema should reflect that immediately.
