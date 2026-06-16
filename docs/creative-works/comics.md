# Comics & Sequential Art

Documentation for the comic book industry, including series, issues, and digital stories.

## Core Types

*   **SequentialArt**: The base type for comics and graphic novels.
*   **ComicSeries**: A series of related comics.
*   **ComicIssue**: A single issue in a comic series.
*   **ComicStory**: An individual story within a comic issue.
*   **ComicCoverArt**: The cover art of a comic.

---

## Comprehensive Example: Comic Issue (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ComicIssue",
  "name": "The Great Adventure #42",
  "issueNumber": "42",
  "datePublished": "2025-06-15",
  "publisher": {
    "@type": "Organization",
    "name": "Global Comics"
  },
  "isPartOf": {
    "@type": "ComicSeries",
    "name": "The Great Adventure"
  },
  "author": [
    {
      "@type": "Person",
      "name": "Aris Thorne",
      "jobTitle": "Writer"
    }
  ],
  "artist": [
    {
      "@type": "Person",
      "name": "Elena Draw",
      "jobTitle": "Illustrator"
    }
  ],
  "colorist": { "@type": "Person", "name": "Charlie Tint" },
  "penciler": { "@type": "Person", "name": "David Line" },
  "letterer": { "@type": "Person", "name": "Eve Type" },
  "hasPart": [
    {
      "@type": "ComicStory",
      "name": "The Hidden Valley",
      "description": "The team discovers a lost world."
    }
  ]
}
```

## Tips for Comics
*   **Specific Roles**: Use `penciler`, `colorist`, `letterer`, and `artist` properties to give full credit to the creative team.
*   **Variant Covers**: Use `workExample` or `hasPart` with `ComicCoverArt` to document different cover versions.
*   **Digital Comics**: Use `SoftwareApplication` or `DigitalDocument` if the comic is specifically an interactive app or a digital file.

## Things to Avoid
*   **Vague Series Info**: Always link an issue back to its `ComicSeries`.
*   **Missing Issue Numbers**: `issueNumber` is vital for cataloging and searching.
