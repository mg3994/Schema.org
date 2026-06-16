# Product Dimensions & Physical Properties

Documentation for describing the physical attributes of a product like weight, height, width, and depth.

## Core Properties

*   **weight**: The weight of the product.
*   **height**: The height of the product.
*   **width**: The width of the product.
*   **depth**: The depth of the product.
*   **model**: The model of the product.
*   **color**: The color of the product.
*   **material**: The material the product is made of.

---

## Comprehensive Example: Product with Physical Dimensions (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Industrial Steel Shelving Unit",
  "description": "Heavy-duty steel shelving for warehouse storage.",
  "weight": {
    "@type": "QuantitativeValue",
    "value": "45.5",
    "unitCode": "KGM"
  },
  "height": {
    "@type": "QuantitativeValue",
    "value": "200",
    "unitCode": "CMT"
  },
  "width": {
    "@type": "QuantitativeValue",
    "value": "120",
    "unitCode": "CMT"
  },
  "depth": {
    "@type": "QuantitativeValue",
    "value": "60",
    "unitCode": "CMT"
  },
  "color": "Silver",
  "material": "Stainless Steel"
}
```

## Tips for Dimensions
*   **Unit Codes**: Always use [UN/CEFACT Common Codes](https://www.unece.org/cefact/codesfortrade/codes_index.html) for `unitCode`.
    *   `KGM` for Kilograms
    *   `LBR` for Pounds
    *   `CMT` for Centimeters
    *   `INH` for Inches
*   **QuantitativeValue**: Using the `@type: QuantitativeValue` object is superior to plain strings as it allows machines to perform unit conversions.
*   **Shipping Weight**: Use `shippingWeight` if the weight for shipping differs from the product's actual weight.

## Things to Avoid
*   **Ambiguous Units**: Don't just write "10 lbs". Use the `unitCode` or `unitText` to be explicit.
*   **Mismatched Dimensions**: Ensure the dimensions match what's in your product manual or visible on the page.
