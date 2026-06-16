# Creative Works Schema Documentation

A `CreativeWork` is the most generic type of creative work, including books, movies, photographs, software programs, etc.

## Major Sub-types

*   [Articles & Postings](articles.md) - News, Blogs, Scholarly articles.
*   [Media Objects](media.md) - Images, Videos, Audio, 3D Models.
*   [Books & Series](books.md) - Books, Audiobooks, Series.
*   [Games & Software](software.md) - Video games, Mobile apps, Web apps.
*   [WebPages & Websites](web.md) - Site structure, FAQ pages, Search results.
*   [Music](music.md) - Recordings, Albums, Compositions.
*   [Visual Arts](visual-arts.md) - Paintings, Sculptures, Drawings.

## Comprehensive List of Types

Below is an exhaustive list of all types falling under `CreativeWork`.

*   **AmpStory**: A story told using the AMP format.
*   **ArchiveComponent**: A component of an archival record.
*   **Article**: Any kind of article (News, Tech, Scholarly, etc.).
*   **Atlas**: A collection of maps.
*   **Blog**: A blog.
*   **Book**: A book.
*   **Certification**: A certification for a product or service.
*   **Chapter**: A chapter of a book.
*   **Claim**: A claim made by someone.
*   **Clip**: A short sequence of video or audio.
*   **Code**: Computer source code.
*   **Collection**: A collection of items.
*   **ComicStory**: A story told in comic format.
*   **Comment**: A comment from a user.
*   **Conversation**: A recorded conversation.
*   **Course**: An educational course.
*   **CreativeWorkSeason**: A season of a series (TV, Radio, Podcast).
*   **CreativeWorkSeries**: A series of creative works.
*   **DataCatalog**: A collection of datasets.
*   **Dataset**: A body of structured information.
*   **DigitalDocument**: A electronic document (PDF, Word, etc.).
*   **Drawing**: A drawing.
*   **Episode**: An episode of a series.
*   **ExercisePlan**: A plan for physical exercise.
*   **Game**: A game (physical or digital).
*   **HowTo**: Instructions for a task.
*   **HyperToc**: A table of contents with hyperlinks.
*   **LearningResource**: A resource for learning.
*   **Legislation**: A law or regulation.
*   **Manuscript**: A handwritten or typed document.
*   **Map**: A map.
*   **Menu**: A menu of food or services.
*   **Message**: A message (Email, SMS).
*   **Movie**: A movie.
*   **MusicComposition**: A musical piece.
*   **MusicPlaylist**: A list of music recordings.
*   **MusicRecording**: A single song or track.
*   **Painting**: A painting.
*   **Photograph**: A photograph.
*   **Play**: A theatrical play.
*   **Poster**: A poster.
*   **PublicationIssue**: An issue of a periodical.
*   **PublicationVolume**: A volume of a periodical.
*   **Quotation**: A quote from someone.
*   **Review**: A review of an item.
*   **Sculpture**: A sculpture.
*   **SheetMusic**: Musical notation.
*   **ShortStory**: A short story.
*   **SoftwareApplication**: A computer program.
*   **SoftwareSourceCode**: Source code of a program.
*   **SpecialAnnouncement**: A timely update (e.g., COVID-19).
*   **Statement**: A formal statement.
*   **Thesis**: An academic thesis.
*   **VisualArtwork**: An artwork (Painting, Sculpture, etc.).
*   **WebContent**: Content on the web.
*   **WebPage**: A single page on the web.
*   **WebPageElement**: An element within a web page (Header, Footer).
*   **WebSite**: A collection of web pages.

---

## Generic CreativeWork Example (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "name": "The Future of AI",
  "author": {
    "@type": "Person",
    "name": "Jane Doe"
  },
  "datePublished": "2025-01-01",
  "description": "An exploration of how AI will shape the next decade.",
  "license": "https://creativecommons.org/licenses/by/4.0/",
  "publisher": {
    "@type": "Organization",
    "name": "Tech Insights"
  }
}
```

## Tips for CreativeWorks
*   **Authorship**: Use the `author` property to connect the work to a `Person` or `Organization`. This builds authority (E-E-A-T).
*   **Licensing**: Always include a `license` property if the work is copyrighted or has a specific usage license.
*   **Citations**: Use the `citation` property to link to other works referenced.
