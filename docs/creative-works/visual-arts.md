# Visual Arts Schema Documentation

Documentation for paintings, sculptures, drawings, and other visual artworks.

## Core Types

*   **VisualArtwork**: The base type for all visual art.
*   **Painting**: A painting.
*   **Sculpture**: A sculpture.
*   **Drawing**: A drawing.
*   **Photograph**: A photograph.

## Specialized Types

*   **CoverArt**: Artwork specifically for a cover (Book, CD).
*   **ComicCoverArt**: Specifically for comics.
*   **Poster**: A poster.

---

## Comprehensive Example: Painting (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Painting",
  "name": "Starry Night",
  "creator": {
    "@type": "Person",
    "name": "Vincent van Gogh"
  },
  "artMedium": "Oil on canvas",
  "artform": "Painting",
  "artworkSurface": "Canvas",
  "width": {
    "@type": "Distance",
    "name": "73.7 cm"
  },
  "height": {
    "@type": "Distance",
    "name": "92.1 cm"
  },
  "dateCreated": "1889",
  "locationCreated": {
    "@type": "Place",
    "name": "Saint-Rémy-de-Provence, France"
  },
  "description": "One of the most recognized paintings in the history of Western culture."
}
```

## Tips for Visual Arts
*   **Dimensions**: Use `width`, `height`, and `depth` (for sculptures) to describe the physical size.
*   **Mediums**: Be descriptive with `artMedium` (e.g., "Bronze", "Digital", "Oil on Wood").
*   **Creators**: Always link to the `Person` who created the work.
*   **Location**: Use `contentLocation` to show where the piece is currently held (e.g., "The Museum of Modern Art").

## Things to Avoid
*   **Missing Dates**: Even an approximate year for `dateCreated` is valuable.
*   **Inconsistent Naming**: Use the title the artist or museum uses.
*   **Confusion between ImageObject and Photograph**: Use `Photograph` for the artistic work and `ImageObject` for the digital file of that work.
