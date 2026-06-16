# Web Page Elements Documentation

Documentation for the technical structure of a web page's layout.

## Core Types

*   **WebPageElement**: The base type for elements within a page.
*   **SiteNavigationElement**: For navigation menus and breadcrumbs.
*   **WPHeader**: The header section of the page.
*   **WPFooter**: The footer section of the page.
*   **WPSideBar**: Sidebar content.
*   **WPAdBlock**: An advertisement block.
*   **Table**: A table structure within the page.

---

## Comprehensive Example: Site Navigation Menu (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "SiteNavigationElement",
  "name": [
    "Home",
    "Services",
    "About Us",
    "Contact"
  ],
  "url": [
    "https://example.com/",
    "https://example.com/services",
    "https://example.com/about",
    "https://example.com/contact"
  ]
}
```

## Tips for Page Elements
*   **Accessibility**: Marking up headers and footers helps assistive technologies understand page structure.
*   **Navigation Hierarchy**: Use `SiteNavigationElement` to explicitly list your primary menu links.
*   **Granularity**: Use `hasPart` within a `WebPage` to link to these elements.

## Things to Avoid
*   **Over-Marking**: Don't mark up every tiny `div`. Focus on the primary structural elements (Header, Footer, Nav, Main).
*   **Hidden Nav**: Ensure the links in `SiteNavigationElement` are actually visible and functional for users.
