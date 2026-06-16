# Entity Linking with @id

One of the most powerful features of JSON-LD is the ability to link entities together using unique identifiers (`@id`). This creates a "Graph" of data, making it easier for search engines to understand the relationships between different entities on your site.

## Why Use @id?

*   **Avoid Redundancy**: Define an organization or person once and reference them everywhere else.
*   **Disambiguation**: Explicitly state that "this" person on page A is the same as "that" person on page B.
*   **Graph Connectivity**: Helps search engines build a Knowledge Graph for your brand.

---

## Comprehensive Example: Linking Author to Organization (JSON-LD)

In this example, we define an `Organization` on the homepage and reference it in an `Article` on a different page.

### On the Homepage (https://example.com/)
```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "@id": "https://example.com/#organization",
  "name": "Tech Insights",
  "url": "https://example.com",
  "logo": "https://example.com/logo.png"
}
```

### On an Article Page (https://example.com/blog/ai-future)
```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "The Future of AI",
  "author": {
    "@type": "Person",
    "name": "Jane Doe",
    "worksFor": { "@id": "https://example.com/#organization" }
  },
  "publisher": { "@id": "https://example.com/#organization" }
}
```

## Tips for Entity Linking
*   **Use Canonical URLs**: The best `@id` is usually the canonical URL of the entity's main page followed by a fragment (e.g., `#organization`, `#person`).
*   **Internal Linking**: Within a single JSON-LD block, you can use relative IDs (e.g., `#author1`) to link properties.
*   **Consistency**: Ensure the `@id` remains stable over time. If the URL changes, update the `@id` everywhere.

## Things to Avoid
*   **Circular References**: Avoid creating infinite loops where A links to B and B links back to A in a way that confuses parsers.
*   **Multiple IDs for One Entity**: Each real-world entity should have exactly one unique `@id` across your entire domain.
*   **Fragile Fragments**: Don't use auto-generated, changing strings for fragments in your `@id`.
