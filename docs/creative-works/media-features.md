# Specialized Media Features

Documentation for interactive and structured media features like video clips and tables of contents.

## Core Types

*   **Clip**: A short sequence of video or audio.
*   **HyperToc**: A structured table of contents for a piece of media or content.
*   **HyperTocEntry**: An individual entry in a `HyperToc`.
*   **MediaReviewItem**: A specific item within a media review.

---

## Comprehensive Example: Video with Key Moments (HyperToc) (JSON-LD)

This example shows how to use `HyperToc` to define specific segments of a video, enabling "Key Moments" in search results.

```json
{
  "@context": "https://schema.org",
  "@type": "VideoObject",
  "name": "Advanced Cooking Techniques",
  "contentUrl": "https://example.com/video.mp4",
  "hasPart": [
    {
      "@type": "Clip",
      "name": "Sautéing Onions",
      "startOffset": 0,
      "endOffset": 120
    },
    {
      "@type": "Clip",
      "name": "Deglazing the Pan",
      "startOffset": 121,
      "endOffset": 300
    }
  ],
  "associatedMedia": {
    "@type": "HyperToc",
    "tocEntry": [
      {
        "@type": "HyperTocEntry",
        "tocContinuation": "https://example.com/video#t=0",
        "utterance": "Introduction to Sautéing"
      },
      {
        "@type": "HyperTocEntry",
        "tocContinuation": "https://example.com/video#t=121",
        "utterance": "Deglazing Techniques"
      }
    ]
  }
}
```

## Tips for Media Features
*   **Offsets**: Use `startOffset` and `endOffset` (in seconds) for `Clip` to define precise segments.
*   **Linking**: Use `tocContinuation` to link a `HyperTocEntry` directly to a timestamped URL.
*   **SEO Impact**: Structured media moments can significantly increase your video's visibility in Google Search and YouTube.

## Things to Avoid
*   **Overlapping Clips**: Ensure `startOffset` and `endOffset` for different clips do not conflict significantly unless intended.
*   **Broken Continuation Links**: Always test timestamped URLs (e.g., `#t=60`) to ensure they work correctly in the player.
