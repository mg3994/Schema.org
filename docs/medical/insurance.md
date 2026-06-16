# Health Plans & Medical Insurance

Documentation for health insurance plans, networks, and cost-sharing details.

## Core Types

*   **HealthInsurancePlan**: A specific health insurance product.
*   **HealthPlanNetwork**: A network of providers for a plan.
*   **HealthPlanCostSharingSpecification**: Details on co-pays and deductibles.
*   **HealthPlanFormulary**: List of covered drugs.

---

## Comprehensive Example: Health Insurance Plan (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "HealthInsurancePlan",
  "name": "Global Shield PPO",
  "healthPlanId": "GSH-2025",
  "usesDevice": "false",
  "benefitsSummaryUrl": "https://example.com/plans/shield-ppo/summary",
  "healthPlanMarketingPriority": "High",
  "includesHealthPlanNetwork": {
    "@type": "HealthPlanNetwork",
    "name": "Global Shield Nationwide Network",
    "healthPlanNetworkId": "GSN-01"
  },
  "includesHealthPlanFormulary": {
    "@type": "HealthPlanFormulary",
    "name": "Shield Preferred Formulary"
  }
}
```

## Tips for Insurance
*   **Unique IDs**: Always include the `healthPlanId`.
*   **Summaries**: Provide a `benefitsSummaryUrl` for user clarity.
*   **Coverage**: Use `areaServed` to show where the insurance plan is available.
*   **Costs**: Use `HealthPlanCostSharingSpecification` for precise co-pay/deductible info.

## Things to Avoid
*   **Ambiguous Terms**: Be precise about whether a plan is PPO, HMO, or EPO in the description.
*   **Outdated Formularies**: Drug coverage changes frequently; keep the `HealthPlanFormulary` link updated.
