# Advanced Developer Patterns

A guide for developers on building scalable and efficient Schema.org implementations using JSON-LD.

## 1. Using @graph for Multiple Entities

Instead of multiple `<script>` tags, you can use an `@graph` array to define multiple entities in a single block. This is cleaner and helps search engines see the relationships instantly.

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://example.com/#org",
      "name": "Acme Corp"
    },
    {
      "@type": "WebSite",
      "@id": "https://example.com/#website",
      "url": "https://example.com",
      "publisher": { "@id": "https://example.com/#org" }
    }
  ]
}
```

## 2. Nesting vs. Linking (via @id)

*   **Nesting**: Good for simple, one-off relationships (e.g., an address inside a business).
*   **Linking**: Better for entities that appear on multiple pages (e.g., the Organization). It reduces payload size and maintenance.

## 3. Dynamic Injection via JavaScript

You can inject JSON-LD dynamically. This is common in Single Page Applications (SPAs).

```javascript
const script = document.createElement('script');
script.type = 'application/ld+json';
const schema = {
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Dynamic Product"
};
script.text = JSON.stringify(schema);
document.head.appendChild(script);
```

## 4. Cleaning the Data

Ensure your JSON-LD does not contain:
*   **Trailing Commas**: These break the parser in older systems.
*   **HTML Entities**: Use UTF-8 characters instead of `&amp;` or `&quot;`.
*   **Invisible Whitespace**: Can occasionally cause parsing errors in specific parsers.

## Tips for Developers
*   **Linter Integration**: Add a JSON-LD validation step to your CI/CD pipeline.
*   **Canonical URLs**: Always use the absolute canonical URL for `@id`.
*   **Conditional Logic**: In your CMS, only output schema for properties that have actual data. Avoid `"sku": ""`.

## Things to Avoid
*   **Payload Bloat**: Don't output the same large Organization block on every single page without using `@id` references.
*   **Blocking Main Thread**: Generating massive JSON-LD blocks on the client-side can occasionally cause layout shifts or performance issues.
