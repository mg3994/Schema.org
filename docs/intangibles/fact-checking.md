# Advanced Reviews & Fact-Checking

Documentation for professional reviews and fact-checking content.

## Core Types

*   **ClaimReview**: A fact-check of a specific claim.
*   **CriticReview**: A professional review of a book, movie, or business.
*   **MediaReview**: A review of a piece of media (image, video).
*   **EmployerReview**: An employee's review of their workplace.

---

## Comprehensive Example: ClaimReview (Fact-Checking) (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ClaimReview",
  "datePublished": "2025-05-10",
  "url": "https://example.com/factcheck/mars-colony",
  "author": {
    "@type": "Organization",
    "name": "Science Verifier"
  },
  "claimReviewed": "The first human colony on Mars will be established by 2026.",
  "reviewRating": {
    "@type": "Rating",
    "ratingValue": "1",
    "bestRating": "5",
    "worstRating": "1",
    "alternateName": "False"
  },
  "itemReviewed": {
    "@type": "CreativeWork",
    "author": {
      "@type": "Person",
      "name": "Anonymous Blogger"
    },
    "datePublished": "2025-05-01"
  }
}
```

## Tips for Advanced Reviews
*   **Rating Alternate Name**: For `ClaimReview`, the `alternateName` (e.g., "False", "True", "Mostly False") is what search engines often display in the Fact Check tag.
*   **ItemReviewed**: Clearly define what is being reviewed. For `CriticReview`, this could be a `Movie`, `Book`, or `Restaurant`.
*   **Trust Building**: Use `author` to link to a professional organization or credentialed individual.

## Things to Avoid
*   **Missing URL**: A review must always point to the original source.
*   **Vague Claims**: The `claimReviewed` should be the exact text or a clear summary of the statement being checked.
