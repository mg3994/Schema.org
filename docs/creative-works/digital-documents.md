# Digital Documents & Code Documentation

Documentation for digital files, source code, and archival components.

## Core Types

*   **DigitalDocument**: A generic digital file (PDF, DOCX, etc.).
*   **NoteDigitalDocument**: A simple digital note.
*   **PresentationDigitalDocument**: A slide presentation.
*   **SpreadsheetDigitalDocument**: A spreadsheet file.
*   **TextDigitalDocument**: A text document.
*   **SoftwareSourceCode**: Computer source code.
*   **ArchiveComponent**: A part of an archival collection.

---

## Comprehensive Example: SoftwareSourceCode (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareSourceCode",
  "name": "Schema-Validator-Utility",
  "description": "A Python utility to validate JSON-LD schema blocks in Markdown files.",
  "programmingLanguage": {
    "@type": "ComputerLanguage",
    "name": "Python"
  },
  "runtimePlatform": "Python 3.10+",
  "codeRepository": "https://github.com/example/schema-validator",
  "targetProduct": {
    "@type": "SoftwareApplication",
    "name": "Schema Validator",
    "operatingSystem": "Linux, Windows, MacOS"
  },
  "license": "https://opensource.org/licenses/MIT",
  "author": {
    "@type": "Person",
    "name": "Jane Developer"
  }
}
```

## Tips for Digital Documents
*   **File Format**: Use `encodingFormat` (MIME type) to specify the file format (e.g., `application/pdf`).
*   **Repository**: For code, always include the `codeRepository` URL.
*   **Languages**: For documents, specify the `inLanguage`.
*   **Permissions**: Use `hasDigitalDocumentPermission` to describe who can access the document.

## Things to Avoid
*   **Missing Licenses**: Always clarify how the code or document can be used.
*   **Broken Repo Links**: Ensure the `codeRepository` points to a valid project page.
