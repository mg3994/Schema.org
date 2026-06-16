# Migration Guide: Microdata to JSON-LD

Many older websites still use Microdata (inline HTML attributes). Moving to JSON-LD is highly recommended for modern SEO and easier maintenance.

## 1. Why Migrate?

*   **Decoupling**: JSON-LD separates data from presentation. You can change your HTML without breaking your schema.
*   **Maintenance**: It's much easier to manage a single script block than hundreds of `itemprop` attributes scattered throughout your HTML.
*   **Google's Preference**: Google has explicitly stated that JSON-LD is the preferred format.

## 2. Migration Steps

### Step 1: Identify Existing Schema
Crawl your site or use the Schema Markup Validator to identify all pages using Microdata.

### Step 2: Map Properties
For each Microdata type (e.g., `Product`), map the existing properties to their JSON-LD equivalents.

**Microdata (Old):**
```html
<div itemscope itemtype="https://schema.org/Product">
  <span itemprop="name">Widget</span>
  <span itemprop="price">$10.00</span>
</div>
```

**JSON-LD (New):**
```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Widget",
  "offers": {
    "@type": "Offer",
    "price": "10.00",
    "priceCurrency": "USD"
  }
}
```

### Step 3: Implementation
Inject the JSON-LD script into the `<head>` of your page.

### Step 4: Removal
Once the JSON-LD is verified, remove the `itemscope`, `itemtype`, and `itemprop` attributes from your HTML to avoid duplicate schema warnings.

## 3. Handling Mixed Formats
It is technically possible to have both Microdata and JSON-LD on the same page, but it is **not recommended**. It can cause "Duplicate Entity" errors in Search Console.

## Tips for Migration
*   **Use @id**: During migration, use consistent `@id` values to ensure search engines recognize the entities are the same.
*   **Test URL by URL**: Start with your highest-traffic pages and verify them in the Rich Results Test.
*   **Linter**: Use a JSON linter to ensure no syntax errors are introduced during the conversion.
