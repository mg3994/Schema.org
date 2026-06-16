# Anatomical Structure & Systems

Documentation for medical and biological anatomy.

## Core Types

*   **AnatomicalStructure**: A physical part of the body (Bones, Organs, Muscles).
*   **AnatomicalSystem**: A functional system of the body (Circulatory, Respiratory).
*   **Joint / Bone / Ligament / Nerve**: Specific types of anatomical structures.
*   **Artery / Vein / LymphaticVessel**: Types of vessels.

---

## Comprehensive Example: AnatomicalSystem (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "AnatomicalSystem",
  "name": "Circulatory System",
  "description": "The system that circulates blood and lymph through the body.",
  "associatedPathophysiology": "Cardiovascular disease",
  "comprisedOf": [
    { "@type": "AnatomicalStructure", "name": "Heart" },
    { "@type": "AnatomicalStructure", "name": "Arteries" },
    { "@type": "AnatomicalStructure", "name": "Veins" }
  ],
  "relatedCondition": [
    { "@type": "MedicalCondition", "name": "Hypertension" }
  ],
  "relatedTherapy": [
    { "@type": "MedicalTherapy", "name": "Exercise" }
  ]
}
```

## Tips for Anatomy
*   **Hierarchy**: Use `comprisedOf` and `partOfSystem` to show how parts fit together.
*   **Connections**: Link anatomical structures to related `MedicalCondition` and `MedicalTherapy` entities.
*   **Imaging**: Use `relatedAnatomicStructure` within a `MedicalImagingTest` to show what was scanned.

## Things to Avoid
*   **Inaccurate Naming**: Use standard medical terminology for names.
*   **Missing Systems**: Always try to specify which `AnatomicalSystem` a structure belongs to.
