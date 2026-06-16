# Movies, TV & Video Content

Documentation for describing movies, television series, and streaming video content.

## Core Types

*   **Movie**: A single film or movie.
*   **TVSeries**: A series of television episodes.
*   **TVSeason**: A specific season of a series.
*   **TVEpisode**: A single episode of a series.
*   **VideoObject**: The technical file or stream (often nested within Movie or Episode).

---

## Comprehensive Example: TV Series with Episodes (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TVSeries",
  "name": "The Code Chronicles",
  "description": "A thrilling series about the history of computer programming.",
  "actor": [
    { "@type": "Person", "name": "Alice Dev" },
    { "@type": "Person", "name": "Bob Syntax" }
  ],
  "director": { "@type": "Person", "name": "Charlie Logic" },
  "numberOfSeasons": 2,
  "startDate": "2024-01-01",
  "containsSeason": [
    {
      "@type": "TVSeason",
      "seasonNumber": 1,
      "numberOfEpisodes": 10,
      "episode": [
        {
          "@type": "TVEpisode",
          "episodeNumber": 1,
          "name": "Hello World",
          "description": "The origins of the first programs."
        }
      ]
    }
  ]
}
```

## Tips for Media Content
*   **Ratings**: Use `aggregateRating` and `contentRating` (e.g., "PG-13", "TV-MA") for compliance and search visibility.
*   **Trailers**: Nest a `VideoObject` as a `trailer` property to show video previews in search results.
*   **Watch Actions**: Use `potentialAction` with `WatchAction` and `EntryPoint` to link directly to streaming services.
*   **Production Details**: Include `productionCompany`, `countryOfOrigin`, and `releasedEvent`.

## Things to Avoid
*   **Missing DatePublished**: For movies, the release date is a primary identifier.
*   **Inconsistent Episode Numbers**: Ensure `episodeNumber` and `seasonNumber` are accurate.
*   **Vague Genres**: Use specific values in the `genre` property (e.g., "Documentary", "Sci-Fi").
