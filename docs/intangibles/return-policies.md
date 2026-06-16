# Merchant Return Policies

Documentation for describing a merchant's return and refund policies, including seasonal overrides.

## Core Types

*   **MerchantReturnPolicy**: The base for return policies.
*   **MerchantReturnPolicySeasonalOverride**: Special return rules for specific times of the year (e.g., Holidays).
*   **MerchantReturnEnumeration**: Types of returns (Finite, Unlimited, Not Permitted).
*   **ReturnFeesEnumeration**: Free, Original shipping, Restocking fees.
*   **ReturnMethodEnumeration**: By mail, In store, At kiosk.

---

## Comprehensive Example: Holiday Return Policy with Override (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MerchantReturnPolicy",
  "name": "Standard 30-Day Policy",
  "applicableCountry": "US",
  "returnPolicyCategory": "https://schema.org/MerchantReturnFiniteReturnWindow",
  "merchantReturnDays": 30,
  "returnMethod": "https://schema.org/ReturnByMail",
  "returnFees": "https://schema.org/FreeReturn",
  "customerRemorseReturnPolicy": "https://schema.org/MerchantReturnFiniteReturnWindow",
  "customerRemorseReturnFees": "https://schema.org/FreeReturn",
  "customerRemorseReturnLabelSource": "https://schema.org/ReturnLabelDownloadAndPrint",
  "returnPolicySeasonalOverride": [
    {
      "@type": "MerchantReturnPolicySeasonalOverride",
      "name": "Holiday Extended Returns",
      "startDate": "2025-11-01",
      "endDate": "2025-12-31",
      "merchantReturnDays": 90,
      "merchantReturnCutoffDate": "2026-01-31"
    }
  ]
}
```

## Tips for Return Policies
*   **Seasonal Rules**: Use `MerchantReturnPolicySeasonalOverride` to automatically handle extended holiday return periods.
*   **Trust Signals**: Showing "Free Returns" directly in search results via this schema can significantly boost CTR.
*   **Links**: Always link the policy to the actual `url` on your website.

## Things to Avoid
*   **Inconsistent Data**: The schema data must match the text on your website's return policy page.
*   **Vague Ranges**: Use `merchantReturnDays` for a precise number.
