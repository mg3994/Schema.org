# Life Sciences & BioChem Documentation

Detailed documentation for biological and chemical entities.

## Core Types

*   **BioChemEntity**: The root for all bio-chemical entities.
*   **ChemicalSubstance**: A specific chemical substance.
*   **Gene**: A functional unit of heredity.
*   **MolecularEntity**: A single molecule.
*   **Protein**: A large biomolecule.
*   **Taxon**: A biological classification unit.

---

## Comprehensive Example: Protein (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Protein",
  "name": "Hemoglobin",
  "description": "The iron-containing oxygen-transport metalloprotein in the red blood cells.",
  "associatedDisease": [
    { "@type": "MedicalCondition", "name": "Sickle Cell Anemia" }
  ],
  "bioChemSimilarity": [
    { "@type": "Protein", "name": "Myoglobin" }
  ],
  "hasBioChemEntityPart": [
    { "@type": "BioChemEntity", "name": "Heme group" }
  ],
  "isEncodedByBioChemEntity": {
    "@type": "Gene",
    "name": "HBB"
  },
  "scientificName": "Hemoglobin A"
}
```

## Tips for Life Sciences
*   **Cross-References**: Link proteins to the genes that encode them using `isEncodedByBioChemEntity`.
*   **Scientific Names**: Always include the `scientificName` alongside the common name.
*   **Associations**: Link biological entities to the diseases they are associated with.
*   **Identifiers**: Use specialized identifiers from databases like UniProt, GenBank, or PubChem.

## Things to Avoid
*   **Mixing Types**: Be precise; don't use `ChemicalSubstance` for a `Protein`.
*   **Outdated Taxonomy**: Keep `Taxon` hierarchies aligned with modern scientific consensus.
