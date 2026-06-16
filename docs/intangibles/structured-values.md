# Structured Values Documentation

Structured values are types that represent a set of properties that together describe a single value.

## Core Types

*   **ContactPoint**: How to contact an organization or person.
*   **PostalAddress**: A physical mailing address.
*   **GeoCoordinates**: Latitude and Longitude.
*   **GeoShape**: Geometric shapes on a map (Circle, Polygon).
*   **MonetaryAmount**: A value of money in a specific currency.
*   **OpeningHoursSpecification**: Specific times when something is open.
*   **PriceSpecification**: Details about a price (Unit price, Delivery charge).
*   **QuantitativeValue**: A value and its unit (Weight, Length).
*   **NutritionInformation**: Nutritional content of a food item.

## Exhaustive List of Types

*   **CDCPMDRecord**: Specialized record for CDC data.
*   **DatedMoneySpecification**: Price at a specific time.
*   **DefinedRegion**: A region defined by postal codes or other criteria.
*   **EngineSpecification**: Details of an engine.
*   **ExchangeRateSpecification**: Currency exchange rates.
*   **InstantaneousEvent / Error**: Represents an event at a point in time or an error.
*   **InteractionCounter**: Counts of interactions (Likes, Views).
*   **OfferShippingDetails**: Details about shipping an offer.
*   **OrderItem**: An item within an order.
*   **OwnershipInfo**: Information about who owns an item.
*   **PostalCodeRangeSpecification**: A range of postal codes.
*   **PropertyValue**: A generic name-value pair.
*   **QuantitativeValueDistribution**: Distribution of values.
*   **RepaymentSpecification**: Details of a loan repayment.
*   **ServicePeriod / ShippingConditions / ShippingDeliveryTime**: Logistics info.
*   **ShippingRateSettings / ShippingService**: Shipping details.
*   **TypeAndQuantityNode**: A type and a quantity.
*   **WarrantyPromise**: Details of a warranty.

---

## Comprehensive Example: QuantitativeValue (JSON-LD)

Used to describe properties like weight or dimensions.

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Super Coffee Beans",
  "weight": {
    "@type": "QuantitativeValue",
    "value": "500",
    "unitCode": "GRM"
  },
  "height": {
    "@type": "QuantitativeValue",
    "value": "20",
    "unitCode": "CMT"
  }
}
```

## Comprehensive Example: NutritionInformation (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "NutritionInformation",
  "calories": "240 calories",
  "fatContent": "9 grams",
  "carbohydrateContent": "35 grams",
  "proteinContent": "5 grams",
  "servingSize": "1 bowl"
}
```

## Tips for Structured Values
*   **Unit Codes**: Use [UN/CEFACT Common Codes](https://www.unece.org/cefact/codesfortrade/codes_index.html) for `unitCode` (e.g., `GRM` for Gram, `CMT` for Centimeter).
*   **Currency**: Always use [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) currency codes (e.g., `USD`, `EUR`).
*   **Nesting**: These values are almost always nested inside other types (e.g., `address` inside `Organization`).

## Things to Avoid
*   **Plain Text instead of Objects**: Don't just use a string for an address; use the `PostalAddress` object.
*   **Missing Units**: A number without a unit is often useless to a machine.
*   **Invalid Unit Codes**: Stick to the standard codes for maximum compatibility.
