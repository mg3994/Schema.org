# Podcasts & Audio Series

Documentation for podcasts, audiobooks, and radio series.

## Core Types

*   **PodcastSeries**: The entire podcast show.
*   **PodcastSeason**: A specific season of a podcast.
*   **PodcastEpisode**: A single audio episode.
*   **AudioObject**: The underlying audio file.

---

## Comprehensive Example: Podcast Episode (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "PodcastEpisode",
  "name": "The Future of Web 3.0",
  "description": "An interview with leading experts on decentralized internet.",
  "episodeNumber": "45",
  "partOfSeries": {
    "@type": "PodcastSeries",
    "name": "Tech Talk Daily",
    "url": "https://example.com/podcasts/tech-talk"
  },
  "associatedMedia": {
    "@type": "AudioObject",
    "contentUrl": "https://example.com/audio/episode45.mp3",
    "duration": "PT45M12S",
    "encodingFormat": "audio/mpeg"
  },
  "author": {
    "@type": "Person",
    "name": "Sarah Host"
  },
  "datePublished": "2025-06-15"
}
```

## Tips for Podcasts
*   **Audio Length**: Always include `duration` in ISO 8601 format.
*   **Direct Audio Links**: Provide the `contentUrl` for the actual MP3/AAC file.
*   **Series Backlink**: Use `partOfSeries` to link the episode to the main show.
*   **Transcripts**: Use the `transcript` property to improve accessibility and SEO for audio content.

## Things to Avoid
*   **Broken Audio Links**: Ensure the `contentUrl` is stable and accessible.
*   **Missing Thumbnails**: Provide a high-quality `image` for the episode or series.
*   **Vague Descriptions**: Include a summary of the topics covered in the episode.
