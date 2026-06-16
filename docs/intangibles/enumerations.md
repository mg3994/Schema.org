# Enumerations Documentation

An `Enumeration` is a list of predefined values. These are used for properties that have a limited set of valid options.

## Core Enumerations

*   **AdultOrientedEnumeration**: Alcohol, Weapons, etc.
*   **BoardingPolicyType**: Group or Zone boarding.
*   **BookFormatType**: Hardcover, Paperback, EBook.
*   **BusinessEntityType**: Types of business entities.
*   **BusinessFunction**: Rental, Sale, Repair.
*   **DayOfWeek**: Monday through Sunday.
*   **DeliveryMethod**: Parcel service, Locker, On-site pickup.
*   **EventAttendanceModeEnumeration**: Online, Offline, Mixed.
*   **ItemAvailability**: InStock, OutOfStock, PreOrder.
*   **LegalValueLevel**: Authoritative, Official, Unofficial.
*   **MapCategoryType**: Parking map, Transit map.
*   **MeasurementTypeEnumeration**: Body measurement, Wearable measurement.
*   **MedicalEnumeration**: Drug cost, Pregnancy category, Specialty.
*   **MerchantReturnEnumeration**: Return window types.
*   **MusicAlbumProductionType**: Studio, Live, Compilation.
*   **MusicAlbumReleaseType**: Album, Single, EP.
*   **OfferItemCondition**: New, Used, Damaged.
*   **PaymentMethodType**: Cash, Credit card, Bank transfer.
*   **PhysicalActivityCategory**: Aerobic, Anaerobic, Strength.
*   **RefundTypeEnumeration**: Full refund, Exchange, Store credit.
*   **RestrictedDiet**: Vegan, Gluten-free, Kosher.
*   **RsvpResponseType**: Yes, No, Maybe.
*   **SizeGroupEnumeration**: Regular, Petite, Plus.
*   **SizeSystemEnumeration**: Imperial, Metric.
*   **StatusEnumeration**: Action status, Event status, Order status.

---

## Comprehensive Example: ItemAvailability & Condition (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Offer",
  "itemCondition": "https://schema.org/NewCondition",
  "availability": "https://schema.org/InStock"
}
```

## Tips for Enumerations
*   **Use URLs**: Use the full URL of the enumeration value (e.g., `https://schema.org/InStock`) instead of just the word "InStock" for better machine readability.
*   **Specific Enums**: Some properties, like `dayOfWeek`, can accept multiple values.
*   **Status Management**: Use the appropriate status enum for `ActionStatusType`, `EventStatusType`, and `OrderStatus`.

## Things to Avoid
*   **Custom Values**: Don't invent your own status names if a standard Schema.org enum exists.
*   **Case Sensitivity**: While often handled, it's best to follow the exact casing used in Schema.org (e.g., `InStock`, not `instock`).
*   **Mixing Enums**: Ensure you are using the correct enum for the specific property (e.g., don't use `EventStatus` for an `Order`).
