# Validation & Troubleshooting

Documentation for testing your schema implementation and fixing common errors.

## Recommended Tools

1.  **[Schema Markup Validator](https://validator.schema.org/)**: The official community tool for checking general Schema.org syntax and structure.
2.  **[Google Rich Results Test](https://search.google.com/test/rich-results)**: Specifically checks if your markup is eligible for Google's rich results (stars, carousels, etc.).
3.  **[Bing Webmaster Tools](https://www.bing.com/webmasters/help/markup-validator-13204221)**: Provides insight into how Bing sees your structured data.
4.  **[Yandex Webmaster](https://webmaster.yandex.com/tools/microtest/)**: Useful for sites targeting the Russian-speaking market.

---

## Common Errors & Solutions

### 1. "Missing Field" (Warning)
*   **Problem**: You missed a recommended (but not required) property like `sku` or `brand`.
*   **Solution**: Add the property if the data is available. Warnings don't block rich results, but they reduce data quality.

### 2. "Invalid Type" (Error)
*   **Problem**: You used a string where an object or enumeration was expected (e.g., `"itemCondition": "New"` instead of `"itemCondition": "https://schema.org/NewCondition"`).
*   **Solution**: Check the expected type on Schema.org and provide the correct object or URL.

### 3. "Duplicate Entity"
*   **Problem**: Multiple plugins or themes are outputting the same schema (e.g., two `Organization` blocks).
*   **Solution**: Consolodate your schema implementation into one source of truth or use `@id` to link them.

### 4. "Parsing Error: Missing ',' or ']'"
*   **Problem**: Your JSON-LD has a syntax error (trailing comma, unclosed bracket).
*   **Solution**: Use a JSON linter or the Schema Markup Validator to find and fix the syntax error.

---

## Troubleshooting Checklist

- [ ] Is the JSON-LD inside a `<script type="application/ld+json">` tag?
- [ ] Does the data in the schema match the visible text on the page?
- [ ] Are you using literal Booleans (`true`/`false`) instead of strings?
- [ ] Is the `datePublished` and `dateModified` in ISO 8601 format?
- [ ] Have you tested the specific URL in Google's Rich Results Test?
