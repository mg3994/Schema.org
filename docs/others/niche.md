# Specialized & Niche Schemas Documentation

This document covers the most specialized and niche areas of Schema.org, ensuring "each and every" type is accounted for.

## 1. BioChemEntity (Life Sciences)
Designed for the life sciences community to describe molecules, proteins, genes, and chemical substances.

*   **ChemicalSubstance**: A chemical substance.
*   **Gene**: A specific gene.
*   **MolecularEntity**: A molecule.
*   **Protein**: A protein.

### Example: Gene (JSON-LD)
```json
{
  "@context": "https://schema.org",
  "@type": "Gene",
  "name": "BRCA1",
  "description": "A gene that provides instructions for making a protein that acts as a tumor suppressor.",
  "identifier": "ENSG00000012048",
  "hasBioPolymerSequence": "..."
}
```

## 2. Taxon (Biology)
Used for biological taxonomy.

*   **Taxon**: A group of organisms (Species, Genus, etc.).

### Example: Taxon (JSON-LD)
```json
{
  "@context": "https://schema.org",
  "@type": "Taxon",
  "name": "Panthera leo",
  "taxonRank": "Species"
}
```

## 3. Specialized Medical Entities
Beyond common conditions, Schema.org covers deep medical structures.

*   **AnatomicalStructure / System**: Veins, Arteries, Nervous System.
*   **MedicalContraindication**: Why not to use a drug.
*   **MedicalGuideline**: Formal recommendations.
*   **MedicalStudy / Trial**: Clinical research.
*   **MedicalTest**: Specialized labs and imaging.

## 4. Technical & Data Schemas
*   **Code / SoftwareSourceCode**: For documenting source code.
*   **Dataset / DataCatalog**: For open data and research datasets.
*   **StatisticalVariable / Observation**: For reporting statistical data.

## 5. Niche Intangibles
*   **ActionAccessSpecification**: Detailed rules on who can do what.
*   **AlignmentObject**: How content aligns with educational frameworks.
*   **BroadcastFrequencySpecification**: Technical radio/TV details.
*   **EntryPoint**: Deep links for actions.
*   **FloorPlan**: Architectural layouts.

---

## The "Everything" Checklist

To ensure we've covered "every" possible use case, remember that Schema.org is built on **Thing**. Any property can technically be added to any type if it's relevant, but sticking to the hierarchy is best practice.

### Common "Missed" Types:
- **Project**: Funding agencies or research projects.
- **Grant**: Monetary awards.
- **SpeakableSpecification**: Identifying content for voice search.
- **HyperToc**: Interactive tables of contents.

### Tips for Niche Schemas:
1.  **Don't Force It**: If a niche schema doesn't fit your data perfectly, look for a slightly broader one.
2.  **Use Extensions**: For highly specialized fields (like Auto or Health), look at the specific extensions like `auto.schema.org` or `health-lifesci.schema.org`.
3.  **Validate**: The more niche the schema, the more likely you are to make a syntax error. Always use the validator.
