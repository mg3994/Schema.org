# Financial Services Schema Documentation

Documentation for financial products like bank accounts, loans, and investment services.

## Core Types

*   **FinancialProduct**: The base for all financial services.
*   **BankAccount**: A savings or checking account.
*   **LoanOrCredit**: Mortgages, credit cards, and personal loans.
*   **InvestmentOrDeposit**: Brokerage accounts and investment funds.
*   **CurrencyConversionService**: Foreign exchange services.
*   **PaymentService**: Services for making payments.

---

## Comprehensive Example: Mortgage Loan (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MortgageLoan",
  "name": "Fixed-Rate Home Loan",
  "amount": {
    "@type": "MonetaryAmount",
    "currency": "USD",
    "value": "500000"
  },
  "loanTerm": {
    "@type": "QuantitativeValue",
    "value": "30",
    "unitCode": "ANN"
  },
  "annualPercentageRate": "6.5",
  "loanRepaymentForm": "Monthly",
  "provider": {
    "@type": "BankOrCreditUnion",
    "name": "Global Mortgages Inc."
  },
  "offers": {
    "@type": "Offer",
    "url": "https://example.com/mortgages/fixed-30",
    "price": "0",
    "priceCurrency": "USD",
    "description": "No application fee for a limited time."
  }
}
```

## Tips for Financial Services
*   **Annual Percentage Rate (APR)**: For loans and credit cards, `annualPercentageRate` is one of the most important properties for transparency and SEO.
*   **Provider Information**: Always link the product to a `BankOrCreditUnion` or a general `Organization`.
*   **Fees**: Use the `feesAndCommissionsSpecification` property to link to detailed fee disclosures.
*   **Location**: Use `areaServed` if the financial product is only available in specific regions.

## Things to Avoid
*   **Misleading Rates**: Ensure the marked-up interest rates match your official disclosures.
*   **Missing Disclaimers**: Include a link to legal disclaimers in the `description`.
*   **Generic FinancialProduct**: Use the most specific type possible (e.g., `CreditCard` vs `FinancialProduct`).
