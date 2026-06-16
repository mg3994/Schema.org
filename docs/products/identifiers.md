# Product Identifiers Documentation

Documentation for unique identifiers that help search engines and marketplaces precisely identify products.

## Core Identifier Properties

*   **gtin**: Global Trade Item Number (covers GTIN-8, GTIN-12, GTIN-13, GTIN-14).
*   **sku**: Stock Keeping Unit.
*   **mpn**: Manufacturer Part Number.
*   **asin**: Amazon Standard Identification Number (Specialized).
*   **productID**: A generic property for any other unique identifier.

---

## Comprehensive Example: Product with Multiple Identifiers (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "SuperLens 50mm f/1.8",
  "brand": {
    "@type": "Brand",
    "name": "OptiCam"
  },
  "gtin13": "4960999665022",
  "sku": "OPT-50-18",
  "mpn": "SL5018-GEN2",
  "productID": "isbn:9780123456789"
}
```

## Tips for Identifiers
*   **GTIN is King**: If you have a GTIN, use it. It is the most powerful identifier for Google Shopping. Use the specific property for the length (`gtin8`, `gtin12`, `gtin13`, or `gtin14`).
*   **Brand Connection**: Identifiers are most effective when combined with the `brand` property.
*   **Manufacturer Part Number**: `mpn` is vital for B2B and technical products where users search for exact part numbers.

## Things to Avoid
*   **Fake Identifiers**: Never invent a GTIN or SKU. If you don't have one, leave it out.
*   **Wrong GTIN Length**: Ensure you use the property that matches the digit count (e.g., `gtin13` for 13 digits).
*   **Duplicate SKUs**: Ensure each unique product (including variants) has its own SKU.
