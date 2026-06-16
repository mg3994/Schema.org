# Social Media & Blogging Schema

Documentation for blog posts, social media updates, and forum discussions.

## Core Types

*   **BlogPosting**: A single post on a blog.
*   **SocialMediaPosting**: A post on a social networking platform.
*   **DiscussionForumPosting**: A post on a forum or discussion board.
*   **LiveBlogPosting**: A blog post that is updated frequently with new content (e.g., live sports or news).

---

## Comprehensive Example: BlogPosting with Author & Comments (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "BlogPosting",
  "headline": "Top 10 Schema Tips for 2025",
  "image": "https://example.com/blog-hero.jpg",
  "author": {
    "@type": "Person",
    "name": "Alex Writer",
    "url": "https://example.com/authors/alex"
  },
  "publisher": {
    "@type": "Organization",
    "name": "SEO Mastery",
    "logo": "https://example.com/logo.png"
  },
  "datePublished": "2025-04-15",
  "dateModified": "2025-04-16",
  "description": "Improve your structured data with these expert tips.",
  "articleBody": "Full content of the blog post goes here...",
  "commentCount": 25,
  "comment": [
    {
      "@type": "Comment",
      "text": "Great article! Very helpful.",
      "author": { "@type": "Person", "name": "Reader A" },
      "dateCreated": "2025-04-15"
    }
  ]
}
```

## Tips for Blogs & Social Media
*   **Live Blogs**: For `LiveBlogPosting`, use the `liveBlogUpdate` property to add individual updates with their own timestamps.
*   **Authorship**: Link the `author` to a verified `Person` profile.
*   **Engagement**: Use `commentCount`, `interactionStatistic` (likes, shares), and `comment` to show social proof.
*   **Modified Date**: Always update `dateModified` to show search engines the content is up-to-date.

## Things to Avoid
*   **Missing Headlines**: Every post needs a clear `headline`.
*   **Generic Authors**: Avoid using "Admin" or "Staff" as the author name; use real names or organization names.
*   **Broken Media**: Ensure `image` URLs are valid and high-quality.
