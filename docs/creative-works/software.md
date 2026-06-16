# Games & Software Documentation

Documentation for video games, mobile applications, and web apps.

## Core Types

*   **SoftwareApplication**: The base type for all software.
*   **MobileApplication**: Specifically for apps on mobile devices.
*   **WebApplication**: For apps that run in a browser.
*   **VideoGame**: Games across all platforms.
*   **Game**: Broad category for any game (physical or digital).

## Specialized Types

*   **SoftwareSourceCode**: Documentation for code itself.
*   **OperatingSystem**: Software that manages hardware.
*   **RuntimePlatform**: A platform on which software runs.

---

## Comprehensive Example: SoftwareApplication (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "TaskMaster Pro",
  "operatingSystem": "iOS, Android",
  "applicationCategory": "ProductivityApplication",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.6",
    "ratingCount": "1200"
  },
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD"
  },
  "downloadUrl": "https://example.com/download",
  "featureList": "Task tracking, team collaboration, sub-tasks, deadline reminders",
  "screenshot": "https://example.com/screenshots/home.png",
  "softwareVersion": "2.1.0"
}
```

## Comprehensive Example: VideoGame (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "VideoGame",
  "name": "Starry Quest",
  "genre": ["RPG", "Space Exploration"],
  "gamePlatform": ["PC", "PlayStation 5", "Xbox Series X"],
  "author": {
    "@type": "Organization",
    "name": "Nebula Games"
  },
  "playMode": "SinglePlayer",
  "trailer": {
    "@type": "VideoObject",
    "name": "Starry Quest Reveal Trailer",
    "embedUrl": "https://example.com/trailers/starry-quest"
  }
}
```

## Tips for Software & Games
*   **Category**: Use the `applicationCategory` property. Common values: `ProductivityApplication`, `GameApplication`, `FinanceApplication`, etc.
*   **Requirements**: Use `memoryRequirements`, `storageRequirements`, and `processorRequirements` for PC software.
*   **Aggregate Rating**: Very important for appearing in app stores and search results with stars.
*   **Platform**: Clearly list all supported `gamePlatform` values.

## Things to Avoid
*   **Vague Categories**: Be as specific as possible with the category.
*   **Old Versions**: Update the `softwareVersion` and `datePublished` when a new update is released.
*   **Missing Screenshots**: Visuals are vital for software documentation.
