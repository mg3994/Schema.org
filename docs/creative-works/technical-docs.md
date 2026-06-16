# Technical API & Code Documentation

Documentation for describing web APIs, source code, and technical documentation components.

## Core Types

*   **WebAPI**: A service providing an interface for programmatic access.
*   **APIReference**: Technical documentation for a specific API.
*   **SoftwareSourceCode**: Documentation for code itself.
*   **Code**: Computer source code.

---

## Comprehensive Example: Web API Documentation (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Global Weather API",
  "description": "Programmatic access to real-time and historical weather data.",
  "documentation": "https://docs.example.com/api",
  "provider": {
    "@type": "Organization",
    "name": "Weather Data Corp"
  },
  "potentialAction": {
    "@type": "SearchAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://api.example.com/v1/weather?q={query}"
    }
  },
  "offers": {
    "@type": "Offer",
    "category": "subscription",
    "priceCurrency": "USD",
    "price": "0.00",
    "description": "Free tier available for up to 1000 requests per month."
  }
}
```

## Tips for Technical Docs
*   **Programming Language**: For code, always specify the `programmingLanguage` (e.g., "Python", "JavaScript").
*   **Repo Links**: Use `codeRepository` to link to GitHub or GitLab.
*   **API Documentation**: Link your `WebAPI` to its `APIReference` pages.
*   **Versions**: Use `softwareVersion` to track API versions.

## Things to Avoid
*   **Broken Endpoint Templates**: Ensure the `urlTemplate` in `SearchAction` is correct.
*   **Missing Licenses**: Always specify the license for source code.
