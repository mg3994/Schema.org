# Business & Education Events

Documentation for conferences, courses, and other professional events.

## Core Types

*   **ConferenceEvent**: Large professional gatherings.
*   **BusinessEvent**: Seminars, workshops.
*   **EducationEvent**: Lectures, school events.
*   **CourseInstance**: A specific instance of a course.
*   **Hackathon**: A coding or creation event.

---

## Comprehensive Example: ConferenceEvent (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ConferenceEvent",
  "name": "Global Tech Summit 2025",
  "startDate": "2025-10-10T09:00:00Z",
  "endDate": "2025-10-12T17:00:00Z",
  "location": {
    "@type": "Place",
    "name": "San Francisco Convention Center",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "San Francisco",
      "addressRegion": "CA"
    }
  },
  "organizer": {
    "@type": "Organization",
    "name": "Tech Events Global"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://example.com/tickets",
    "price": "499.00",
    "priceCurrency": "USD"
  }
}
```

## Tips
*   **Keynote Speakers**: Use the `performer` property to list keynote speakers.
*   **Agenda**: Use `subEvent` to list specific sessions within a conference.

## Things to Avoid
*   **Vague Descriptions**: Be clear about what the event covers.
*   **Missing Timezones**: Always include the timezone in `startDate`.
