# Specialized & Niche Events

Documentation for specific event types like literary readings, comedy shows, and store sales.

## Core Types

*   **LiteraryEvent**: Book readings, poetry slams, and author signings.
*   **ComedyEvent**: Stand-up, improv, and sketch comedy.
*   **SaleEvent**: Limited-time sales and promotions.
*   **ScreeningEvent**: Movie or documentary screenings.
*   **DeliveryEvent**: The event of delivering an item.
*   **Hackathon**: Coding or project-based creation events.

---

## Comprehensive Example: Literary Event (Author Signing) (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "LiteraryEvent",
  "name": "An Evening with Aris Thorne",
  "description": "A reading and signing of the new book 'Mars 2030'.",
  "startDate": "2025-09-20T19:00:00Z",
  "location": {
    "@type": "BookStore",
    "name": "The Open Page",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "123 Story Lane",
      "addressLocality": "Austin"
    }
  },
  "performer": {
    "@type": "Person",
    "name": "Aris Thorne",
    "jobTitle": "Author"
  },
  "workPerformed": {
    "@type": "Book",
    "name": "Mars 2030"
  },
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock"
  }
}
```

## Tips for Specialized Events
*   **Performers**: Always specify the `performer` (Author, Comedian, etc.).
*   **Work Performed**: For screenings and readings, use `workPerformed` to link to the `Movie` or `Book`.
*   **Sub-Events**: For large events like a Hackathon or a Festival, use `subEvent` to list specific workshops or sessions.

## Things to Avoid
*   **Vague Start Times**: Be precise with time and timezone.
*   **Missing Venue Details**: Provide a full `Place` object for the `location`.
*   **Outdated Sale Events**: Ensure `SaleEvent` markup is removed as soon as the sale ends.
