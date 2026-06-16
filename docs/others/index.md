# Specialized & Other Schemas Documentation

This section covers niche Schema.org types that don't fit into the major categories but are essential for specific industries.

## 1. BioChemEntity
Used for describing biological and chemical entities.
*   **ChemicalSubstance**: A chemical substance.
*   **Gene**: A specific gene.
*   **MolecularEntity**: A molecule.
*   **Protein**: A protein.

## 2. Taxon
Used for biological taxonomy.
*   **Taxon**: A group of organisms (Species, Genus, etc.).
*   **childTaxon / parentTaxon**: To show hierarchy.

---

## Comprehensive Example: Taxon (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Taxon",
  "name": "Panthera leo",
  "taxonRank": "Species",
  "alternateName": "Lion",
  "parentTaxon": {
    "@type": "Taxon",
    "name": "Panthera",
    "taxonRank": "Genus"
  },
  "sameAs": "https://www.wikidata.org/wiki/Q8939"
}
```

## 3. Data Types
While not "Schemas" in the sense of entities, these are the building blocks of all property values.
*   **Boolean**: True/False.
*   **Date / DateTime / Time**: Time-related values.
*   **Number / Integer / Float**: Numerical values.
*   **Quantity**: Distance, Duration, Energy, Mass.
*   **Text**: URL, CssSelectorType, XPathType.

---

## Final Thoughts on "Covering Everything"

Schema.org is a living vocabulary. While this documentation covers all current top-level types and their hierarchies as of early 2025, always check the [official Schema.org release notes](https://schema.org/docs/releases.html) for the latest additions.

### Core Architecture Reminder:
1.  **Thing**: The root of everything.
2.  **Types**: Categories of things (e.g., `Person`).
3.  **Properties**: Attributes of types (e.g., `name`).
4.  **DataTypes**: The type of value a property can have (e.g., `Text`).

By combining these, you can describe almost anything in the digital and physical world in a way that machines can understand.
