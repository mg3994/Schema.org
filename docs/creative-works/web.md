# WebPages & Websites Documentation

Documentation for structure of the web itself.

## Core Types

*   **WebSite**: A set of related web pages and other items typically served from a single web domain and accessible via URLs.
*   **WebPage**: Every page on your site should be a `WebPage` or one of its subtypes.
*   **WebPageElement**: Parts of a page like headers, footers, and sidebars.

## Specialized WebPage Types

*   **AboutPage**: Information about the site or entity.
*   **CheckoutPage**: The page where users pay.
*   **CollectionPage**: A page containing a collection of items (e.g., product gallery).
*   **ContactPage**: Page for contact info.
*   **FAQPage**: Page with Frequently Asked Questions.
*   **ItemPage**: A page about a single item.
*   **MedicalWebPage**: Web page with medical info.
*   **ProfilePage**: Page about a person or organization.
*   **QAPage**: A page with questions and their answers.
*   **RealEstateListing**: A page listing property for sale/rent.
*   **SearchResultsPage**: Page showing results for a query.

---

## Comprehensive Example: FAQPage (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "How do I implement Schema.org?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "You can implement Schema.org using JSON-LD, Microdata, or RDFa. JSON-LD is the recommended format."
    }
  }, {
    "@type": "Question",
    "name": "Is JSON-LD better than Microdata?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "Yes, for most use cases, JSON-LD is easier to maintain and preferred by Google."
    }
  }]
}
```

## Comprehensive Example: WebSite with Search Action

```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "url": "https://www.example.com/",
  "potentialAction": {
    "@type": "SearchAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://query.example.com/search?q={search_term_string}"
    },
    "query-input": "required name=search_term_string"
  }
}
```

## Tips for Web Schema
*   **Sitelinks Searchbox**: Implement the `WebSite` search action to enable the search box within Google's search results for your site.
*   **Breadcrumbs**: Always use `BreadcrumbList` on every sub-page to help search engines understand site hierarchy.
*   **MainEntity**: Use `mainEntity` to specify the primary thing the page is about.
*   **Navigation**: Use `SiteNavigationElement` to mark up your primary menu.

## Things to Avoid
*   **Broken Search Templates**: Ensure the `urlTemplate` for `SearchAction` is correct and handles the placeholder.
*   **FAQ Misuse**: Only use `FAQPage` for content that is strictly formatted as Questions and Answers.
*   **Missing About/Contact Pages**: Explicitly marking these up helps establish trust and authority.
