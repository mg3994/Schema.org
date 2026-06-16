# Internationalization (i18n) & Schema

Handling multi-language and multi-region content is a common challenge for global websites. Schema.org provides several ways to manage this complexity.

## Core Properties for i18n

*   **inLanguage**: The language of the content (use BCP 47 codes like `en-US` or `fr-FR`).
*   **availableLanguage**: Languages supported by a service or person.
*   **areaServed**: The geographic area where a service is provided.
*   **workTranslation**: Linking a work to its translations.

---

## Comprehensive Example: Multi-language Article (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "The Future of Space Exploration",
  "inLanguage": "en-US",
  "workTranslation": [
    {
      "@type": "Article",
      "headline": "El futuro de la exploración espacial",
      "inLanguage": "es-ES",
      "url": "https://example.com/es/blog/futuro-espacio"
    },
    {
      "@type": "Article",
      "headline": "L'avenir de l'exploration spatiale",
      "inLanguage": "fr-FR",
      "url": "https://example.com/fr/blog/avenir-espace"
    }
  ]
}
```

## Tips for Global Schema
*   **Use BCP 47**: Always follow the standard for language codes (e.g., `pt-BR` for Brazilian Portuguese).
*   **Cross-Link Translations**: Use the `workTranslation` or `translationOfWork` properties to connect different versions of the same piece of content.
*   **Specify Regions**: For businesses, use `areaServed` with `Country` or `AdministrativeArea` objects.
*   **Currency Matching**: Ensure the `priceCurrency` matches the region and language of the offer.

## Things to Avoid
*   **Mismatched Content**: Don't put Spanish metadata on an English-language page.
*   **Generic Language Codes**: Use specific regional codes if the content is tailored (e.g., `zh-HK` vs `zh-CN`).
*   **Ignoring Local Laws**: Some regions have specific requirements for how certain data (like medical or legal) must be presented.
