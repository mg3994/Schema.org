# Ratings & Reviews Documentation

Documentation for user reviews and aggregate ratings.

## Core Types

*   **Review**: A single review from a person.
*   **AggregateRating**: The average rating based on multiple reviews.
*   **ClaimReview**: A review of a claim (fact-checking).
*   **CriticReview**: A review by a professional critic.
*   **EmployerReview**: A review of an employer by an employee.
*   **MediaReview**: A review of a media item (Video, Image).
*   **Recommendation**: A recommendation for an item.

---

## Comprehensive Example: AggregateRating (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Elite Wireless Headphones",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.5",
    "reviewCount": "120",
    "bestRating": "5",
    "worstRating": "1"
  }
}
```

## Tips for Reviews
*   **Scales**: Always specify `bestRating` and `worstRating` if they are not the default 1 and 5.
*   **Authors**: Every `Review` should have an `author` (a `Person` or `Organization`).
*   **Fact Checking**: Use `ClaimReview` for fact-checking content to get the "Fact Check" tag in search results.
*   **Visibility**: Ensure the reviews you mark up are actually visible to users on the page.

## Things to Avoid
*   **Fake Reviews**: Do not mark up reviews that were not actually provided by users.
*   **Review Snippets without Full Text**: Google prefers seeing the actual review text.
*   **Irrelevant Reviews**: Ensure reviews are for the specific product or entity on the page.
