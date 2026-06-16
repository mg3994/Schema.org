# Schema Implementation FAQ

Frequently Asked Questions about implementing and managing Schema.org structured data.

---

### Q: Where should I place my JSON-LD script?
**A:** You can place it in the `<head>` or the `<body>` of your HTML. Google recommends the `<head>` for faster discovery, but either works.

### Q: Can I have more than one JSON-LD block on a page?
**A:** Yes. You can have multiple `<script>` tags. However, it is often cleaner to combine related entities into a single graph using an `@graph` array or linking them via `@id`.

### Q: Does Schema.org improve my rankings?
**A:** Not directly. Structured data is not a ranking signal. However, it *indirectly* improves SEO by making your site eligible for rich results (stars, images, etc.), which significantly increases Click-Through Rate (CTR).

### Q: Should I mark up every single page?
**A:** Yes, if the page contains a primary entity (Product, Article, LocalBusiness, etc.). Even simple pages can benefit from `BreadcrumbList` or `WebPage` schema.

### Q: How often does Google update my rich results?
**A:** It depends on how often your site is crawled. It can take anywhere from a few hours to several weeks after you update your schema for the changes to appear in search results.

### Q: What if my data doesn't fit any Schema.org type?
**A:** Use the most specific type that *partially* fits, or use `Thing` with the `additionalType` property to link to an external vocabulary like Wikipedia or an industry-specific ontology.

### Q: Is Microdata better than JSON-LD?
**A:** No. Google strongly prefers JSON-LD because it is easier to maintain and doesn't clutter your HTML. Use JSON-LD whenever possible.

### Q: Can I use Schema for hidden content?
**A:** No. Generally, you should only mark up content that is visible to the user. Marking up hidden content can lead to a manual action from search engines.

---

## Still have questions?
Check out the [official Schema.org Documentation](https://schema.org/docs/documents.html) or the [Google Search Central forums](https://developers.google.com/search/community).
