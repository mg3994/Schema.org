# Medical & Health Schema Documentation

`MedicalEntity` is the root for all medical-related schemas. This vocabulary is extremely detailed and intended for health providers, researchers, and medical websites.

## Major Categories

*   **AnatomicalStructure**: Bones, Muscles, Organs, Vessels.
*   **AnatomicalSystem**: Respiratory, Circulatory, etc.
*   **MedicalCondition**: Diseases, Symptoms, Signs.
*   **MedicalProcedure**: Surgeries, Tests, Exams.
*   **MedicalStudy**: Clinical trials, Observational studies.
*   **MedicalTest**: Blood tests, Imaging tests.
*   **Substance**: Drugs, Dietary supplements.
*   **MedicalGuideline**: Recommendations and contraindications.
*   **LifestyleModification**: Diets, Exercise plans.

## Exhaustive List of Types

*   **Bone / BrainStructure / Joint / Ligament / Muscle / Nerve**: Anatomical structures.
*   **Artery / LymphaticVessel / Vein**: Types of vessels.
*   **DrugClass / DrugCost**: Drug-related info.
*   **InfectiousDisease**: Specific types of conditions.
*   **MedicalSign / MedicalSymptom / VitalSign**: Signs and symptoms.
*   **DiagnosticProcedure / SurgicalProcedure / TherapeuticProcedure**: Procedures.
*   **OccupationalTherapy / PhysicalTherapy / RadiationTherapy**: Therapies.
*   **MedicalRiskCalculator / MedicalRiskScore**: Risk estimators.
*   **MedicalObservationalStudy / MedicalTrial**: Types of studies.
*   **BloodTest / ImagingTest / PathologyTest**: Types of tests.
*   **DietarySupplement / Drug**: Substances.
*   **SuperficialAnatomy**: Surface level anatomy.
*   **MedicalCode**: Coding systems like ICD-10 or SNOMED.

---

## Comprehensive Example: MedicalCondition (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalCondition",
  "name": "Type 2 Diabetes",
  "description": "A chronic condition that affects the way the body processes blood sugar (glucose).",
  "code": {
    "@type": "MedicalCode",
    "codeValue": "E11",
    "codingSystem": "ICD-10"
  },
  "associatedAnatomy": {
    "@type": "AnatomicalStructure",
    "name": "Pancreas"
  },
  "possibleSymptom": [
    { "@type": "MedicalSymptom", "name": "Increased thirst" },
    { "@type": "MedicalSymptom", "name": "Frequent urination" }
  ],
  "possibleTreatment": [
    { "@type": "LifestyleModification", "name": "Healthy eating" },
    { "@type": "LifestyleModification", "name": "Regular exercise" },
    { "@type": "Drug", "name": "Metformin" }
  ],
  "drug": {
    "@type": "Drug",
    "name": "Metformin"
  },
  "primaryPrevention": {
    "@type": "LifestyleModification",
    "name": "Weight management"
  }
}
```

## Tips for Medical Schema
*   **Coding Systems**: Use `MedicalCode` to map your conditions and procedures to international standards (ICD-10, MeSH, SNOMED). This is high-level data that search engines trust.
*   **Authority**: Ensure the `publisher` or `author` of medical content is a verified medical professional or organization (YMYL - Your Money Your Life).
*   **Contraindications**: For drugs and procedures, always include `contraindication` info for safety.
*   **Associated Anatomy**: Link conditions to the parts of the body they affect.

## Things to Avoid
*   **Medical Advice**: Always include a disclaimer that the information is for informational purposes only.
*   **Unverified Claims**: Don't mark up "cures" or treatments that are not scientifically backed.
*   **Missing Status**: For clinical trials, always keep the `status` (Recruiting, Completed, etc.) up to date.
