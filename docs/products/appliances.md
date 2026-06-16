# Energy Efficiency & Appliances

Documentation for describing energy consumption and efficiency of products and appliances.

## Core Properties

*   **hasEnergyConsumptionDetails**: Container for energy usage information.
*   **energyEfficiencyScaleMin / max**: The scale used for energy ratings.
*   **energyStarCertified**: Boolean indicating Energy Star certification.
*   **energyEfficiencyCategory**: The category on the efficiency scale (e.g., "A+++").

---

## Comprehensive Example: Energy Efficient Refrigerator (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "EcoChill Smart Refrigerator",
  "category": "Household Appliance",
  "hasEnergyConsumptionDetails": {
    "@type": "EnergyConsumptionDetails",
    "energyEfficiencyCategory": "https://schema.org/EUEnergyEfficiencyCategoryA3Plus",
    "energyStarCertified": true
  },
  "offers": {
    "@type": "Offer",
    "price": "1200.00",
    "priceCurrency": "USD"
  }
}
```

## Tips for Appliances
*   **Energy Star**: Always use the `energyStarCertified` property if applicable, as it is a major search filter for eco-conscious consumers.
*   **Specific Categories**: Use the full Schema.org URL for energy efficiency categories (e.g., from the `EUEnergyEfficiencyEnumeration`).
*   **Voltage and Power**: Use `QuantitativeValue` to describe voltage or wattage requirements if they are critical for the product description.

## Things to Avoid
*   **Confusing Scales**: Be clear about which efficiency scale is being used (EU vs US Energy Star).
*   **Missing Certification Data**: Certification data should be verifiable.
