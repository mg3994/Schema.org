# Introduction to Schema.org & Best Practices (2025)

Schema.org is a collaborative, community activity with a mission to create, maintain, and promote schemas for structured data on the Internet. In 2025, structured data is more critical than ever, powering not just search engine rich results but also AI-driven discovery and data parsing.

## General Principles

### 1. JSON-LD is King
While Schema.org supports Microdata and RDFa, **JSON-LD (JavaScript Object Notation for Linked Data)** is the industry standard and Google's strongly preferred format.
*   **Cleaner HTML**: It keeps your data separate from your presentation layer.
*   **Easier Maintenance**: Easier to generate dynamically from a CMS.
*   **Asynchronous**: Can be injected via JavaScript without blocking page render.

### 2. Consistency is Crucial
The data in your schema **must match** the visible content on the page. Discrepancies can lead to manual actions or loss of rich result eligibility.

### 3. Use Unique IDs (@id)
Whenever possible, use a stable `@id` (usually the canonical URL of the entity) to disambiguate entities. This allows you to reference the same entity across multiple pages without redefining it.

---

## Tips & Tricks

*   **Nesting vs. Linking**: Nest related entities (e.g., a `Person` inside an `Article` as an `author`) to provide clear context.
*   **SameAs Property**: Use `sameAs` to link your entities to authoritative sources like Wikipedia, Wikidata, or official social media profiles. This helps search engines disambiguate who or what you are talking about.
*   **Image Dimensions**: For `ImageObject`, always include `width` and `height` to help platforms render previews correctly.
*   **Date Formats**: Always use ISO 8601 format for dates and times (e.g., `2025-06-15T10:00:00Z`).

---

## Things to Avoid (Common Pitfalls)

*   **Hidden Markup**: Don't mark up content that is hidden from users (unless it's necessary for the machine to understand the visible content).
*   **Generic Types**: Don't use `Thing` if a more specific type like `Product` or `Event` exists. Be as specific as possible.
*   **Duplicate Schema**: Avoid having multiple plugins or themes outputting conflicting schema for the same entity. Use one source of truth.
*   **Ignoring Errors**: Check your implementation using the [Schema Markup Validator](https://validator.schema.org/) and [Google's Rich Results Test](https://search.google.com/test/rich-results).
*   **Outdated Properties**: Schema.org evolves. Avoid deprecated properties (e.g., `speakable` was deprecated in some contexts; check the latest docs).

---

## The Golden Rule
**If it's visible to the user, mark it up. If it's not visible, don't invent it.**
