# Music Schema Documentation

Documentation for music recordings, albums, and compositions.

## Core Types

*   **MusicRecording**: A single track or song.
*   **MusicAlbum**: A collection of recordings.
*   **MusicPlaylist**: A user-defined or curated list of tracks.
*   **MusicComposition**: The underlying musical work (score/lyrics).
*   **MusicRelease**: A specific release of an album or track.

## Specialized Types

*   **MusicGroup**: A band or orchestra.
*   **MusicVideoObject**: A video of a musical performance.

---

## Comprehensive Example: MusicAlbum (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MusicAlbum",
  "name": "Neon Dreams",
  "byArtist": {
    "@type": "MusicGroup",
    "name": "The Synth-Waves"
  },
  "albumProductionType": "https://schema.org/StudioAlbum",
  "albumReleaseType": "https://schema.org/AlbumRelease",
  "genre": "Synth-pop",
  "datePublished": "2025-05-20",
  "numTracks": 10,
  "track": [
    {
      "@type": "MusicRecording",
      "position": 1,
      "name": "Midnight Drive",
      "duration": "PT4M12S"
    },
    {
      "@type": "MusicRecording",
      "position": 2,
      "name": "Electric Sky",
      "duration": "PT3M45S"
    }
  ]
}
```

## Tips for Music Schema
*   **ISRC**: For `MusicRecording`, always include the ISRC (International Standard Recording Code).
*   **Durations**: Use ISO 8601 duration format (e.g., `PT3M45S`).
*   **Hierarchy**: A `MusicAlbum` should contain a list of `MusicRecording` in the `track` property.
*   **Artists**: Link back to the `MusicGroup` or `Person` who created the work.

## Things to Avoid
*   **Generic Genres**: Use specific genres for better classification.
*   **Incorrect Track Order**: Ensure the `position` matches the actual track listing on the album.
*   **Missing Release Date**: Crucial for sorting and "New Release" features.
