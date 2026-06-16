# Detailed BioChem & Molecular Schema

Exhaustive documentation for describing chemical substances, molecules, proteins, and genes.

## Core Types

*   **BioChemEntity**: The root for all biochemical entities.
*   **ChemicalSubstance**: A specific chemical substance (e.g., Aspirin).
*   **MolecularEntity**: A single molecule or ion.
*   **Protein**: A large biomolecule consisting of one or more chains of amino acid residues.
*   **Gene**: A locus of DNA which is made up of nucleotides.

---

## Comprehensive Example: Chemical Substance (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ChemicalSubstance",
  "name": "Ascorbic Acid",
  "alternateName": "Vitamin C",
  "chemicalComposition": "C6H8O6",
  "molecularWeight": "176.12 g/mol",
  "identifier": "CID 5467006",
  "potentialUse": "Antioxidant",
  "sameAs": "https://pubchem.ncbi.nlm.nih.gov/compound/Ascorbic-acid"
}
```

## Comprehensive Example: Gene & Protein Link (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Gene",
      "@id": "https://example.org/genes/INS",
      "name": "INS",
      "description": "Insulin gene.",
      "isEncodedByBioChemEntity": { "@id": "https://example.org/proteins/Insulin" }
    },
    {
      "@type": "Protein",
      "@id": "https://example.org/proteins/Insulin",
      "name": "Insulin",
      "description": "A peptide hormone produced by beta cells of the pancreatic islets."
    }
  ]
}
```

## Tips for BioChem
*   **Registry IDs**: Use identifiers from authoritative databases like PubChem, UniProt, or Ensembl.
*   **SameAs Linking**: Always use `sameAs` to point to the canonical entry in scientific databases.
*   **Sequences**: Use `hasBioPolymerSequence` for proteins and genes.
*   **Anatomy**: Link proteins to the `AnatomicalStructure` where they are primarily produced.

## Things to Avoid
*   **Inaccurate Formulas**: Double-check the `chemicalComposition`.
*   **Generic Types**: Don't use `Thing` when `MolecularEntity` or `Protein` is applicable.
