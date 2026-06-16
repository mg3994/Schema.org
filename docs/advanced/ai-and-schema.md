# Schema.org & AI (LLMs / Agents)

In 2025, Schema.org is no longer just for Google Search. It has become the "language of the web" for Artificial Intelligence, including Large Language Models (LLMs) and autonomous agents.

## How AI Uses Schema.org

1.  **Contextual Understanding**: LLMs use structured data to better understand the relationships between facts, entities, and actions.
2.  **Autonomous Actions**: AI agents use `PotentialAction` schema to understand how to interact with your site (e.g., "How do I book a flight?").
3.  **Data Extraction**: Schema makes it 100x easier for AI to scrape and parse your data accurately without hallucinating details.
4.  **Retrieval Augmented Generation (RAG)**: Better schema means better indexing for RAG systems, leading to more accurate AI-generated answers about your brand.

---

## Example: Documenting an AI-Friendly Action (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "AI Assistant Pro",
  "potentialAction": {
    "@type": "BuyAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://example.com/checkout?id=ai-pro",
      "actionPlatform": [
        "http://schema.org/DesktopWebPlatform",
        "http://schema.org/MobileWebPlatform"
      ]
    },
    "price": "99.00",
    "priceCurrency": "USD"
  }
}
```

## Best Practices for AI-Ready Schema
*   **Be Verbose**: Don't just provide the minimum required fields. The more properties you provide, the better an LLM can understand your entity.
*   **Use SameAs**: Connect your entities to Wikidata and Wikipedia. This allows AI to cross-reference your data with global knowledge bases.
*   **Explicit Actions**: Use `PotentialAction` for every meaningful task a user (or agent) can perform on your site.
*   **Keep it Fresh**: AI models value recent data. Ensure `dateModified` is always accurate.

## Things to Avoid
*   **Confusing Ambiguity**: Avoid using generic types like `Thing` or `CreativeWork` when more specific types exist.
*   **Inconsistent Logic**: Ensure that the logical flow of your data (e.g., an `Event` happening at a `Place`) makes sense.
*   **Blocking Scrapers**: If you want AI to use your schema, ensure your JSON-LD blocks are not blocked by robots.txt or heavy obfuscation.
