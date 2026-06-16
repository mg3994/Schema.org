# Books & Series Documentation

Documentation for books, audiobooks, and various types of series.

## Core Types

*   **Book**: A book.
*   **Audiobook**: An audio version of a book.
*   **CreativeWorkSeries**: A series of creative works.
*   **BookSeries**: A series of books.
*   **MovieSeries**: A series of movies.
*   **TVSeries**: A television series.
*   **PodcastSeries**: A series of podcasts.

## Specialized Types

*   **Chapter**: A chapter of a book.
*   **SequentialArt**: Comics, graphic novels.
*   **ComicSeries**: A series of comics.
*   **Newspaper**: A periodical publication.
*   **Periodical**: A publication that comes out on a regular basis.

---

## Comprehensive Example: Book with Offers (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Book",
  "name": "The Great Gatsby",
  "author": {
    "@type": "Person",
    "name": "F. Scott Fitzgerald"
  },
  "isbn": "9780743273565",
  "bookFormat": "https://schema.org/Hardcover",
  "numberOfPages": 180,
  "datePublished": "1925-04-10",
  "publisher": {
    "@type": "Organization",
    "name": "Charles Scribner's Sons"
  },
  "workExample": [
    {
      "@type": "Book",
      "bookFormat": "https://schema.org/EBook",
      "isbn": "9780743273565",
      "potentialAction": {
        "@type": "ReadAction",
        "target": {
          "@type": "EntryPoint",
          "urlTemplate": "https://example.com/read/gatsby"
        }
      }
    }
  ]
}
```

## Tips for Books & Series
*   **ISBN**: Always include the ISBN-13 for books.
*   **Work vs. Instance**: Use `workExample` to link the abstract "Work" to specific versions (Hardcover, EBook, Audiobook).
*   **Series Hierarchy**: For TV or Podcast series, use `hasPart` to link to `CreativeWorkSeason`, and then to `Episode`.
*   **Format**: Use the `bookFormat` property with values from the `BookFormatType` enumeration.

## Things to Avoid
*   **Missing Authors**: A book should always have an `author`.
*   **Confusing Series**: Don't confuse a `CreativeWorkSeries` (the whole show) with a `CreativeWorkSeason` (one year) or an `Episode` (one show).
*   **Invalid ISBN**: Ensure the ISBN is a valid 10 or 13 digit number.
