# Grants & Funding Documentation

Documentation for describing monetary and non-monetary grants, and the schemes that provide them.

## Core Types

*   **Grant**: A grant, typically financial or academic.
*   **MonetaryGrant**: Specifically for financial grants.
*   **FundingScheme**: A scheme for providing funds (e.g., a specific grant program).
*   **FundingAgency**: An organization that provides funding.

---

## Comprehensive Example: MonetaryGrant (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MonetaryGrant",
  "name": "Innovation Research Grant 2025",
  "description": "A grant for small businesses developing green technology.",
  "amount": {
    "@type": "MonetaryAmount",
    "currency": "USD",
    "value": "50000"
  },
  "funder": {
    "@type": "FundingAgency",
    "name": "Federal Tech Foundation"
  },
  "recipient": {
    "@type": "Organization",
    "name": "GreenTech Solutions"
  },
  "isBasedOn": {
    "@type": "FundingScheme",
    "name": "Small Business Innovation Research (SBIR)"
  }
}
```

## Tips for Grants
*   **Funder and Recipient**: Always clearly identify both the `funder` and the `recipient`.
*   **Amount**: Use the `MonetaryAmount` type for financial values.
*   **Scheme**: Link the grant to its parent `FundingScheme`.
*   **Sponsorship**: For research projects or publications, use the `funder` property on those types.

## Things to Avoid
*   **Vague Amounts**: Be precise about the currency and value.
*   **Missing Status**: If a grant is "Pending" or "Awarded", use the description or a status property if applicable.
