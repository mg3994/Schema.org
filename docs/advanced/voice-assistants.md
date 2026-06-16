# Voice Assistants & Speakable Schema

Documentation for optimizing content for voice assistants like Alexa, Google Assistant, and Siri using Schema.org.

## Core Types

*   **SpeakableSpecification**: Identifies sections of a page that are particularly appropriate for text-to-speech conversion.

## Core Properties

*   **cssSelector**: Selecting elements via CSS.
*   **xpath**: Selecting elements via XPath.

---

## Comprehensive Example: Speakable News Article (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "NewsArticle",
  "headline": "New Mars Discovery",
  "speakable": {
    "@type": "SpeakableSpecification",
    "cssSelector": [
      ".article-headline",
      ".article-summary"
    ]
  },
  "url": "https://example.com/news/mars"
}
```

## Tips for Voice Optimization
*   **Concise Summaries**: Choose sections that provide a clear, concise summary of the page's main point.
*   **Technical Identifiers**: Use stable CSS classes or IDs (e.g., `#voice-summary`) to avoid breaking the schema when layout changes.
*   **News Focus**: Currently, the `speakable` property is most widely supported for `NewsArticle` types.
*   **Accessibility Summary**: Combine with `accessibilitySummary` on `WebPage` to help assistive technologies.

## Things to Avoid
*   **Selecting the Whole Page**: Don't mark up the entire page as speakable; it leads to a poor user experience.
*   **Non-Text Content**: Avoid selecting elements that contain complex tables, advertisements, or navigation links.
*   **Mismatched Content**: Ensure the selected text is actually readable and makes sense in a voice context.
