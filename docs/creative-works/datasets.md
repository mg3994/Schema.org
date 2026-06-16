# Datasets & Data Science Documentation

Documentation for datasets, catalogs, and data feeds. This is critical for scientific research, open data portals, and data-driven applications.

## Core Types

*   **Dataset**: A body of structured information.
*   **DataCatalog**: A collection of datasets.
*   **DataFeed**: A data feed, which is periodically updated.
*   **CompleteDataFeed**: A data feed that represents the complete state of the data.

---

## Comprehensive Example: Dataset (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Dataset",
  "name": "Global Surface Temperatures 1880-2025",
  "description": "Historical data of global surface temperature anomalies.",
  "url": "https://example.org/datasets/temp-data",
  "identifier": "https://doi.org/10.1234/dataset.5678",
  "keywords": ["climate", "temperature", "global warming", "environment"],
  "creator": {
    "@type": "Organization",
    "name": "Global Climate Institute"
  },
  "distribution": [
    {
      "@type": "DataDownload",
      "encodingFormat": "text/csv",
      "contentUrl": "https://example.org/downloads/temp-data.csv"
    },
    {
      "@type": "DataDownload",
      "encodingFormat": "application/json",
      "contentUrl": "https://example.org/downloads/temp-data.json"
    }
  ],
  "license": "https://creativecommons.org/licenses/by/4.0/",
  "temporalCoverage": "1880-01-01/2025-12-31",
  "spatialCoverage": {
    "@type": "Place",
    "name": "Global"
  }
}
```

## Tips for Datasets
*   **DOI**: Use the `identifier` property to provide a DOI (Digital Object Identifier).
*   **Distributions**: Provide multiple `distribution` objects for different file formats (CSV, JSON, XML).
*   **Coverage**: Clearly define `temporalCoverage` and `spatialCoverage` so researchers can find relevant data.
*   **Variable Measured**: Use `variableMeasured` to describe the specific variables in the dataset.

## Things to Avoid
*   **Broken Downloads**: Ensure `contentUrl` is always a direct link to the file.
*   **Missing License**: Always specify the `license` to inform users of how they can use the data.
*   **Vague Descriptions**: A dataset's description should clearly state what data it contains and how it was collected.
