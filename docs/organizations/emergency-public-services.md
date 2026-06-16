# Emergency & Public Services

Documentation for local and national public services, including emergency responders and government offices.

## Core Types

*   **EmergencyService**: The base type for responders.
*   **PoliceStation**: A local police office.
*   **FireStation**: A local fire department.
*   **Hospital**: A medical facility providing emergency and inpatient care.
*   **Embassy**: A diplomatic mission.
*   **CityHall**: The administrative center of a city.
*   **Courthouse**: A building where legal trials are held.

---

## Comprehensive Example: Police Station with Emergency Action (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "PoliceStation",
  "name": "Central Police Station",
  "telephone": "+15559110000",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "100 Justice Way",
    "addressLocality": "Springfield",
    "addressRegion": "IL"
  },
  "openingHours": "Mo-Su 00:00-23:59",
  "potentialAction": {
    "@type": "InformAction",
    "name": "Report an Emergency",
    "recipient": {
      "@type": "EmergencyService",
      "name": "Dispatch Center"
    }
  }
}
```

## Tips for Public Services
*   **24/7 Availability**: Most emergency services are open 24/7; represent this clearly with `openingHours: "Mo-Su 00:00-23:59"`.
*   **Emergency Phone**: Use a dedicated `telephone` property for emergency contact if it differs from the administrative line.
*   **Jurisdiction**: For City Halls and Courthouses, use `areaServed` to show the administrative reach.

## Things to Avoid
*   **Missing Addresses**: Public service buildings are primary landmarks; a full `PostalAddress` and `geo` coordinates are essential.
*   **Vague Naming**: Use the official municipal or departmental name.
