# Lifestyle & Wellness Schema

Documentation for diets, physical activities, and exercise plans.

## Core Types

*   **LifestyleModification**: The base for wellness-related changes.
*   **Diet**: A specific dietary plan (Vegan, Keto, etc.).
*   **PhysicalActivity**: A category of exercise (Aerobic, Strength).
*   **ExercisePlan**: A detailed plan for physical activity.

---

## Comprehensive Example: Exercise Plan (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ExercisePlan",
  "name": "30-Day Strength Starter",
  "description": "A beginner-friendly plan to build functional strength.",
  "duration": "P30D",
  "exerciseType": "Strength training",
  "intensity": "Moderate",
  "repetitionFrequency": "3 times per week",
  "restPeriods": "PT1M",
  "workload": {
    "@type": "QuantitativeValue",
    "value": "45",
    "unitText": "minutes"
  },
  "author": {
    "@type": "Person",
    "name": "Coach Iron"
  }
}
```

## Comprehensive Example: Diet (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Diet",
  "name": "Plant-Based Performance",
  "description": "A high-protein vegan diet for athletes.",
  "dietFeatures": "High protein, whole foods, no refined sugars.",
  "expertConsiderations": "Ensure adequate B12 intake.",
  "associatedDisease": {
    "@type": "MedicalCondition",
    "name": "Hypertension"
  }
}
```

## Tips for Wellness
*   **Intensity**: Use `intensity` (Low, Moderate, High) to help users find appropriate plans.
*   **Durations**: Use ISO 8601 for `duration` (e.g., `P30D` for 30 days) and `restPeriods`.
*   **Experts**: Link the author to a `Person` with relevant credentials.
*   **Medical Context**: Use `associatedDisease` to show if a diet or exercise is helpful for specific conditions.

## Things to Avoid
*   **Medical Advice Disclaimer**: Always include a disclaimer that the plan is not a substitute for professional medical advice.
*   **Vague Instructions**: Be as specific as possible about repetitions, rest, and duration.
