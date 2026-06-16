# Medical Treatments & Procedures

Documentation for surgeries, therapies, drugs, and lifestyle modifications.

## Core Types

*   **Drug**: Pharmaceutical treatments.
*   **MedicalTherapy**: Physical therapy, occupational therapy.
*   **SurgicalProcedure**: Operations.
*   **LifestyleModification**: Diets and exercise.
*   **TherapeuticProcedure**: General therapeutic actions.

---

## Comprehensive Example: Drug (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Drug",
  "name": "Ibuprofen",
  "activeIngredient": "Ibuprofen",
  "dosageForm": "Tablet",
  "drugPrescriptionStatus": "https://schema.org/OTC",
  "isProprietary": "false",
  "legalStatus": {
    "@type": "DrugLegalStatus",
    "applicableLocation": { "@type": "Country", "name": "US" }
  },
  "maximumIntake": {
    "@type": "DoseSchedule",
    "maximumDailyDose": "1200 mg"
  },
  "overdosage": "Seek immediate medical attention if overdose is suspected.",
  "pregnancyCategory": "https://schema.org/FDAcategoryC"
}
```

## Tips for Treatments
*   **Active Ingredients**: Always specify the `activeIngredient`.
*   **Legal Status**: Use `legalStatus` to show if a drug is Prescription-only or OTC.
*   **Dosage**: Use `doseSchedule` for detailed dosage info.

## Things to Avoid
*   **Ignoring Side Effects**: Always mention potential side effects or contraindications.
*   **Incorrect Pregnancy Category**: This is critical for safety; ensure it matches FDA or local equivalents.
