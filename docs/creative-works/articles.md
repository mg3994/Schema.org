# Articles & Postings Documentation

Articles include news reports, blog posts, scholarly articles, and social media postings.

## Core Types

*   **Article**: The most generic article type.
*   **NewsArticle**: An article reporting on news.
*   **BlogPosting**: A post on a blog.
*   **ScholarlyArticle**: An article in an academic journal.
*   **TechArticle**: An article about a technical subject (API docs, tutorials).
*   **SocialMediaPosting**: A post on a social network.

## Exhaustive Sub-types

*   **AdvertiserContentArticle**: Sponsored content.
*   **AnalysisNewsArticle**: In-depth news analysis.
*   **AskPublicNewsArticle**: Q&A style news.
*   **BackgroundNewsArticle**: Background info on a news event.
*   **OpinionNewsArticle**: Opinion pieces.
*   **ReportageNewsArticle**: On-the-ground reporting.
*   **ReviewNewsArticle**: A news article that is also a review.
*   **SatiricalArticle**: Satire.
*   **MedicalScholarlyArticle**: Medical academic research.
*   **LiveBlogPosting**: A blog post updated in real-time.
*   **DiscussionForumPosting**: A post on a forum.
*   **APIReference**: Technical documentation for an API.

---

## Comprehensive Example: NewsArticle (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "NewsArticle",
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://example.com/news/future-of-space"
  },
  "headline": "Humanity's Next Giant Leap: Mars 2030",
  "image": [
    "https://example.com/photos/1x1/photo.jpg",
    "https://example.com/photos/4x3/photo.jpg",
    "https://example.com/photos/16x9/photo.jpg"
  ],
  "datePublished": "2025-02-15T08:00:00+08:00",
  "dateModified": "2025-02-15T09:20:00+08:00",
  "author": [{
    "@type": "Person",
    "name": "Dr. Aris Thorne",
    "url": "https://example.com/authors/aris-thorne",
    "jobTitle": "Lead Astrophysicist"
  }],
  "publisher": {
    "@type": "Organization",
    "name": "Galactic News",
    "logo": {
      "@type": "ImageObject",
      "url": "https://example.com/logo.png"
    }
  },
  "description": "An in-depth look at the upcoming Mars mission and the technology behind it.",
  "articleBody": "Content of the article goes here...",
  "keywords": ["Mars", "Space Exploration", "NASA", "2030"],
  "isAccessibleForFree": true,
  "hasPart": {
    "@type": "WebPageElement",
    "isAccessibleForFree": false,
    "cssSelector": ".premium-content"
  }
}
```

## Tips & Tricks for Articles
*   **Headlines**: Keep your `headline` concise and matching the H1 of the page.
*   **DateModified**: Always update `dateModified` when you make significant changes to the content. Search engines love fresh data.
*   **Multiple Authors**: Use an array for the `author` property if there are multiple contributors.
*   **Paywalls**: Use the `isAccessibleForFree` and `hasPart` properties to correctly mark up paywalled content, helping search engines understand which parts are locked.

## Things to Avoid
*   **Fake Dates**: Never put a future date in `datePublished`.
*   **Mismatched Content**: The `articleBody` in your schema should be a faithful representation of the text on the page.
*   **Broken Logos**: Ensure the `publisher.logo` URL is valid and the image meets size requirements (usually 600px wide for Google).
