# People Schema Documentation

The `Person` type represents an individual, alive, dead, undead, or fictional.

## Major Sub-types

*   **Patient**: A person who receives medical care.

---

## Comprehensive Example: Person (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Sarah J. Miller",
  "alternateName": "Sarah Miller",
  "jobTitle": "Chief Technology Officer",
  "worksFor": {
    "@type": "Organization",
    "name": "Global Tech Corp"
  },
  "url": "https://www.sarahjmiller.me",
  "image": "https://www.sarahjmiller.me/sarah.jpg",
  "sameAs": [
    "https://www.linkedin.com/in/sarahjmiller",
    "https://twitter.com/sarahjmiller",
    "https://github.com/sarahjmiller"
  ],
  "alumniOf": {
    "@type": "CollegeOrUniversity",
    "name": "Stanford University",
    "sameAs": "https://en.wikipedia.org/wiki/Stanford_University"
  },
  "knowsAbout": ["Artificial Intelligence", "Cloud Computing", "Ethics in Tech"],
  "description": "Sarah is a seasoned CTO with over 20 years of experience in the tech industry.",
  "givenName": "Sarah",
  "familyName": "Miller",
  "honorificPrefix": "Dr.",
  "gender": "Female",
  "nationality": {
    "@type": "Country",
    "name": "USA"
  }
}
```

## Tips for Person Schema
*   **E-E-A-T Building**: Using `Person` schema for authors of articles is critical for Google's E-E-A-T (Experience, Expertise, Authoritativeness, and Trustworthiness) signals.
*   **KnowsAbout**: Use the `knowsAbout` property to list specific areas of expertise. This helps search engines understand what the person is an expert in.
*   **SameAs**: Link to social profiles and personal websites to prove that this person is a real, verifiable entity.
*   **Job Titles & Affiliations**: Always include `jobTitle` and `worksFor` to provide professional context.

## Things to Avoid
*   **Private Info**: Avoid marking up sensitive private information like personal phone numbers or home addresses unless intended for public consumption.
*   **Incomplete Names**: Use `givenName` and `familyName` separately for better parsing.
*   **Overuse**: Don't mark up every single mention of a person on a page; focus on the primary entities (author, interviewee, founder).
