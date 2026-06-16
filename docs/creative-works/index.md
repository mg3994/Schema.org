# Creative Works Schema Documentation

A `CreativeWork` is the most generic type of creative work.

## Detailed Guides

*   [Articles & Postings](articles.md) - News, Blogs, Scholarly articles.
*   [Media Objects](media.md) - Images, Videos, Audio, 3D Models.
*   [Books & Series](books.md) - Books, Audiobooks, Series.
*   [Games & Software](software.md) - Video games, Mobile apps, Web apps.
*   [WebPages & Websites](web.md) - Site structure, FAQ pages, Search results.
*   [Music](music.md) - Recordings, Albums, Compositions.
*   [Visual Arts](visual-arts.md) - Paintings, Sculptures, Drawings.
*   [Datasets & Data Science](datasets.md) - Datasets, DataCatalogs, DataFeeds.
*   [Recipes & How-To](how-to-recipes.md) - Cooking recipes, DIY guides.
*   [Digital Documents & Code](digital-documents.md) - Files, Source code.
*   [Movies, TV & Video](movies-tv.md) - Films, Series, and Episodes.
*   [Podcasts & Audio](podcasts.md) - Audio shows and episodes.
*   [Specialized Works](specialized.md) - Comics, Theses, and Reports.
*   [Social Media & Blogging](social-media.md) - Blog posts and social updates.
*   [Web Page Elements](page-elements.md) - Headers, Footers, and Navigation.

## Core Example (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "name": "General Creative Work",
  "author": { "@type": "Person", "name": "Jane Doe" }
}
```
