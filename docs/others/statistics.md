# Statistics & Data Populations

Documentation for describing statistical data, variables, and populations. Essential for researchers and data scientists.

## Core Types

*   **StatisticalVariable**: A specific variable being measured (e.g., "Median Household Income").
*   **Observation**: A single data point or measurement.
*   **StatisticalPopulation**: The group being studied (e.g., "Citizens of New York City").
*   **QuantitativeValueDistribution**: How values are distributed across a population.

---

## Comprehensive Example: Household Income Statistics (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Observation",
  "name": "Median Household Income 2024",
  "observationAbout": {
    "@type": "StatisticalPopulation",
    "name": "Households in Illinois",
    "address": {
      "@type": "PostalAddress",
      "addressRegion": "IL"
    }
  },
  "measuredVariable": {
    "@type": "StatisticalVariable",
    "name": "Median Household Income"
  },
  "measuredValue": {
    "@type": "MonetaryAmount",
    "currency": "USD",
    "value": "75000"
  },
  "observationDate": "2024-12-31",
  "marginOfError": {
    "@type": "QuantitativeValue",
    "value": "1200",
    "unitCode": "USD"
  }
}
```

## Tips for Statistics
*   **Precision**: Use `measuredValue` and `marginOfError` for technical accuracy.
*   **Temporal Coverage**: Always specify the `observationDate` or `temporalCoverage`.
*   **Population Specifics**: Use `StatisticalPopulation` to define exactly who or what is included in the data set.

## Things to Avoid
*   **Vague Variables**: Be explicit about what is being measured (e.g., "Mean" vs "Median").
*   **Missing Units**: A value without a unit (Currency, Percentage) is ambiguous.
