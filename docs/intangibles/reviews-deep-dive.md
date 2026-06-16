# Advanced Deep Dive into Reviews

Expanding documentation for user-generated reviews, employer reviews, and professional recommendations.

## Core Types

*   **UserReview**: A review created by a non-professional user.
*   **EmployerReview**: A review of an organization by an employee (past or present).
*   **Recommendation**: A recommendation for an entity (Place, Person, Product).
*   **EndorsementRating**: A rating based on an endorsement.

---

## Comprehensive Example: Employer Review (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "EmployerReview",
  "name": "Excellent Culture at TechFlow",
  "itemReviewed": {
    "@type": "Organization",
    "name": "TechFlow Systems"
  },
  "reviewRating": {
    "@type": "Rating",
    "ratingValue": "5"
  },
  "author": {
    "@type": "Person",
    "name": "Anonymous Employee"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Job Portal Elite"
  },
  "reviewBody": "Great work-life balance and high growth potential.",
  "datePublished": "2025-02-15"
}
```

## Comprehensive Example: Recommendation (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Recommendation",
  "category": "Travel",
  "itemReviewed": {
    "@type": "Hotel",
    "name": "The Grand Azure"
  },
  "reviewRating": {
    "@type": "Rating",
    "ratingValue": "5"
  },
  "author": {
    "@type": "Person",
    "name": "Jane Travel-Guide"
  },
  "recommendationScore": "9.8"
}
```

## Tips for Advanced Reviews
*   **Scales**: Always specify `bestRating` and `worstRating` if the scale is not 1-5.
*   **ItemReviewed**: This must be a specific Schema.org type (e.g., `Product`, `LocalBusiness`, `CreativeWork`).
*   **Review Body**: Ensure the `reviewBody` contains the actual text of the review.
*   **Employer Specifics**: For `EmployerReview`, use properties like `jobTitle` (linked via `author`) to provide context.

## Things to Avoid
*   **Spam Reviews**: Only mark up genuine reviews. Search engines penalize fraudulent review schema.
*   **Vague Targets**: Be explicit about exactly which branch or office is being reviewed if it's a large organization.
