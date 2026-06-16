# Medical Studies & Tests

Documentation for clinical research, observational studies, and medical diagnostic tests.

## Core Types

*   **MedicalStudy**: The base type for all medical research.
*   **MedicalTrial**: A clinical trial (interventional).
*   **MedicalObservationalStudy**: A study that observes subjects without intervention.
*   **MedicalTest**: Any medical diagnostic test.
*   **BloodTest / ImagingTest / PathologyTest**: Specific test types.

---

## Comprehensive Example: Clinical Trial (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalTrial",
  "name": "Phase III Study of New Diabetic Drug",
  "description": "Evaluating the efficacy and safety of Drug-X in patients with Type 2 Diabetes.",
  "status": "https://schema.org/Recruiting",
  "phase": "Phase III",
  "trialDesign": "https://schema.org/RandomizedTrial",
  "sponsor": {
    "@type": "Organization",
    "name": "Global Pharma Research"
  },
  "studySubject": {
    "@type": "MedicalCondition",
    "name": "Type 2 Diabetes"
  },
  "healthCondition": {
    "@type": "MedicalCondition",
    "name": "Type 2 Diabetes"
  },
  "objectives": "To measure the reduction in HbA1c levels over 52 weeks."
}
```

## Tips for Research & Tests
*   **Status**: Use the `MedicalStudyStatus` enumeration (Recruiting, Completed, Withdrawn).
*   **Trial Phase**: Be explicit about the phase (Phase I-IV).
*   **Sponsors**: Identifying the research `sponsor` or `principalInvestigator` builds trust.
*   **Test Results**: Use `normalRange` and `significance` properties for diagnostic tests.

## Things to Avoid
*   **Outdated Status**: Keep the recruiting status updated.
*   **Missing Subject Info**: Always specify the condition or population being studied.
*   **Ambiguous Designs**: Use the `MedicalTrialDesign` enumeration values.
