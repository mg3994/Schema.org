# Specialized Structured Values

Documentation for niche structured values used in specific technical or financial contexts.

## Core Types

*   **EngineSpecification**: Detailed specifications for a vehicle engine (Displacement, Fuel type, Horsepower).
*   **RepaymentSpecification**: Details for loan or credit repayments.
*   **DatedMoneySpecification**: The value of money at a specific point in time.
*   **LocationFeatureSpecification**: Features of a place (Wi-Fi, parking, accessibility).

---

## Comprehensive Example: Engine Specification (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "EngineSpecification",
  "name": "V6 Turbo Diesel",
  "engineType": "Diesel",
  "engineDisplacement": {
    "@type": "QuantitativeValue",
    "value": "3.0",
    "unitCode": "LTR"
  },
  "enginePower": {
    "@type": "QuantitativeValue",
    "value": "250",
    "unitCode": "HP"
  },
  "torque": {
    "@type": "QuantitativeValue",
    "value": "600",
    "unitCode": "NMT"
  }
}
```

---

## Comprehensive Example: Repayment Specification (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "RepaymentSpecification",
  "numberOfRepayments": 36,
  "repaymentFrequency": "Monthly",
  "downPayment": {
    "@type": "MonetaryAmount",
    "value": "2000",
    "currency": "USD"
  },
  "loanPaymentAmount": {
    "@type": "MonetaryAmount",
    "value": "350",
    "currency": "USD"
  }
}
```

## Tips for Specialized Values
*   **Unit Precision**: For engines, use `LTR` (liters), `HP` (horsepower), and `NMT` (newton meters).
*   **Frequency**: For repayments, common values are `Monthly`, `Weekly`, `Yearly`.
*   **Nesting**: These types are almost always nested inside larger types like `Vehicle` or `LoanOrCredit`.

## Things to Avoid
*   **Mixed Units**: Don't mix metric and imperial units in the same object if possible.
*   **Vague Frequencies**: Be precise about when payments are due.
