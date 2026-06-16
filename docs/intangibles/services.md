# Services & Reservations Documentation

Documentation for services provided and the act of reserving them.

## Core Types

### Services
*   **Service**: The base type for services.
*   **BroadcastService / RadioBroadcastService**: Media services.
*   **FinancialProduct / BankAccount / LoanOrCredit**: Financial services.
*   **FoodService**: Restaurant or catering services.
*   **GovernmentService**: Public services.
*   **TaxiService**: Transport services.
*   **WebAPI**: A web-based API service.

### Reservations
*   **Reservation**: The base for all bookings.
*   **BoatReservation / BusReservation / TrainReservation**: Transport bookings.
*   **FlightReservation**: Airline bookings.
*   **FoodEstablishmentReservation**: Restaurant bookings.
*   **LodgingReservation**: Hotel or rental bookings.
*   **RentalCarReservation**: Car rental bookings.
*   **ReservationPackage**: A group of related reservations.

---

## Comprehensive Example: FinancialProduct (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "InvestmentOrDeposit",
  "name": "High-Yield Savings Account",
  "annualPercentageYield": "4.5",
  "amount": {
    "@type": "MonetaryAmount",
    "currency": "USD",
    "value": "1000"
  },
  "provider": {
    "@type": "BankOrCreditUnion",
    "name": "Global Bank"
  }
}
```

## Tips for Services & Reservations
*   **Providers**: Use the `provider` property to identify the organization offering the service.
*   **Service Type**: Be specific with `serviceType`.
*   **Reservation Status**: Use the `ReservationStatusType` enumeration.
*   **Confirmation**: Always include a `reservationId` for confirmed bookings.

## Things to Avoid
*   **Missing Providers**: A service must always have a provider.
*   **Vague Terms**: Clearly define the terms of the reservation (Check-in time, Cancellation policy).
