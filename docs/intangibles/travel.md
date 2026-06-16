# Travel & Logistics Schema Documentation

Documentation for trips, flights, and travel reservations.

## Core Types

*   **Trip**: A journey from one place to another.
*   **Flight**: A specific flight between two airports.
*   **BusTrip / TrainTrip / BoatTrip**: Other forms of transit journeys.
*   **TouristTrip**: A sightseeing trip or tour.
*   **TouristDestination**: A destination for tourists.

---

## Comprehensive Example: Flight with Details (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Flight",
  "flightNumber": "AA123",
  "provider": {
    "@type": "Airline",
    "name": "Global Airways",
    "iataCode": "GA"
  },
  "departureAirport": {
    "@type": "Airport",
    "name": "JFK International Airport",
    "iataCode": "JFK"
  },
  "arrivalAirport": {
    "@type": "Airport",
    "name": "London Heathrow",
    "iataCode": "LHR"
  },
  "departureTime": "2025-12-15T22:00:00Z",
  "arrivalTime": "2025-12-16T10:00:00Z",
  "webCheckinTime": "2025-12-14T22:00:00Z",
  "offers": {
    "@type": "Offer",
    "price": "550.00",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock"
  }
}
```

## Tips for Travel
*   **IATA Codes**: Always use standard IATA codes for `Airport` and `Airline` objects.
*   **Timezones**: Use ISO 8601 with timezone offsets or UTC (Z) for all departure and arrival times.
*   **Tourist Destinations**: For attractions, link to the `TouristDestination` type.
*   **Reservations**: Combine with `FlightReservation` for booking confirmations.

## Things to Avoid
*   **Missing Time Data**: A flight without departure/arrival times is not useful.
*   **Incorrect Codes**: Double-check IATA/ICAO codes for accuracy.
*   **Confusing Trip with Event**: A `Trip` is a journey, while a `Festival` or `Conference` is an `Event`.
