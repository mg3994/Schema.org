# Medical Conditions & Diseases

Detailed documentation for marking up medical conditions, diseases, and health concerns.

## Core Properties

*   **associatedAnatomy**: Body parts affected.
*   **possibleSymptom**: Common symptoms.
*   **possibleTreatment**: Potential treatments.
*   **riskFactor**: Things that increase the chance of getting the condition.
*   **differentialDiagnosis**: Other conditions with similar symptoms.
*   **naturalProgression**: How the condition evolves if untreated.
*   **status**: Current state (e.g., Chronic, Acute).

---

## Comprehensive Example: Infectious Disease (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "InfectiousDisease",
  "name": "Influenza",
  "description": "A viral infection that attacks your respiratory system.",
  "infectiousAgent": "Influenza virus",
  "transmissionMethod": "Airborne droplets",
  "incubationPeriod": "P1D to P4D",
  "possibleSymptom": [
    { "@type": "MedicalSymptom", "name": "Fever" },
    { "@type": "MedicalSymptom", "name": "Cough" },
    { "@type": "MedicalSymptom", "name": "Fatigue" }
  ],
  "associatedAnatomy": {
    "@type": "AnatomicalSystem",
    "name": "Respiratory System"
  }
}
```

## Tips for Conditions
*   **Specificity**: Use `InfectiousDisease` instead of `MedicalCondition` when applicable.
*   **Timelines**: Use `incubationPeriod` for infectious diseases.
*   **Anatomy Connection**: Always link the condition to the affected body part or system.

## Things to Avoid
*   **Guaranteed Cures**: Avoid using language that suggests a treatment is a guaranteed cure.
*   **Missing Professional Review**: Ensure medical content is reviewed by a professional.
