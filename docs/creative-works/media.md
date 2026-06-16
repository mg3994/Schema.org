# Media Objects Documentation

Media objects represent various types of digital media like images, videos, audio, and documents.

## Core Types

*   **ImageObject**: An image file.
*   **VideoObject**: A video file.
*   **AudioObject**: An audio file.
*   **DataDownload**: A dataset download.
*   **3DModel**: A 3D graphical model.

## Specialized Types

*   **Barcode**: An image of a barcode.
*   **MusicVideoObject**: A music video.
*   **TextObject**: A text-based media object.
*   **LegislationObject**: A legal document in digital form.
*   **Audiobook**: A digital recording of a book.
*   **MediaObjectSnapshot**: A snapshot of a media object at a point in time (e.g., `VideoObjectSnapshot`).

---

## Comprehensive Example: VideoObject (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "VideoObject",
  "name": "How to Bake a Sourdough Loaf",
  "description": "A step-by-step guide to making professional-grade sourdough at home.",
  "thumbnailUrl": [
    "https://example.com/thumbnails/123.jpg"
  ],
  "uploadDate": "2025-03-10T12:00:00Z",
  "duration": "PT12M30S",
  "contentUrl": "https://example.com/videos/sourdough-tutorial.mp4",
  "embedUrl": "https://example.com/embed/sourdough-tutorial",
  "interactionStatistic": {
    "@type": "InteractionCounter",
    "interactionType": { "@type": "WatchAction" },
    "userInteractionCount": 15400
  },
  "regionsAllowed": ["US", "CA", "GB"],
  "hasPart": [
    {
      "@type": "Clip",
      "name": "Preparing the Starter",
      "startOffset": 0,
      "endOffset": 180,
      "url": "https://example.com/videos/sourdough-tutorial#t=0"
    },
    {
      "@type": "Clip",
      "name": "Mixing the Dough",
      "startOffset": 181,
      "endOffset": 400,
      "url": "https://example.com/videos/sourdough-tutorial#t=181"
    }
  ]
}
```

## Tips for Media Objects
*   **Thumbnails**: Always provide multiple thumbnail URLs in different ratios (1:1, 4:3, 16:9).
*   **ISO 8601 Duration**: Ensure `duration` is in the correct format (e.g., `PT1M30S` for 1 minute 30 seconds).
*   **Clips**: Use the `hasPart` property with `Clip` types to enable "Key Moments" in Google Search results.
*   **Transcript**: For video and audio, providing a `transcript` property is excellent for accessibility and SEO.

## Things to Avoid
*   **Dead Links**: Ensure `contentUrl` and `embedUrl` are always active.
*   **Low Resolution**: Avoid small thumbnails; high-quality images improve click-through rates.
*   **Inaccurate Timestamps**: Double-check your `Clip` offsets; they must be accurate to the second.
