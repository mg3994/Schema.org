# Vehicle Schema Documentation

The `Vehicle` type and its sub-types (Car, Bus, Motorcycle) are used for describing motorized transport.

## Core Types

*   **Car**: A conventional automobile.
*   **Motorcycle**: A two-wheeled vehicle.
*   **BusOrCoach**: Large transport vehicles.
*   **MotorizedBicycle**: E-bikes.

---

## Comprehensive Example: Car (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Car",
  "name": "2024 Model X Electric",
  "brand": {
    "@type": "Brand",
    "name": "VoltMotors"
  },
  "vehicleModelDate": "2024",
  "vehicleEngine": {
    "@type": "EngineSpecification",
    "engineType": "Electric",
    "enginePower": {
      "@type": "QuantitativeValue",
      "value": "450",
      "unitCode": "HP"
    }
  },
  "fuelType": "Electric",
  "numberOfDoors": 5,
  "seatingCapacity": 5,
  "bodyType": "SUV",
  "color": "Midnight Blue",
  "mileageFromOdometer": {
    "@type": "QuantitativeValue",
    "value": "1200",
    "unitCode": "SMI"
  },
  "vin": "1ABC23456789DEFG"
}
```

## Tips for Vehicles
*   **VIN**: For specific used vehicles, include the `vin` (Vehicle Identification Number).
*   **Mileage**: Use `mileageFromOdometer` for used vehicles.
*   **Engine Details**: Use `vehicleEngine` to provide technical specs.
*   **Fuel Type**: Specify `Electric`, `Gasoline`, `Diesel`, or `Hybrid`.

## Things to Avoid
*   **Missing Model Year**: `vehicleModelDate` is a primary search filter for users.
*   **Generic Body Types**: Be specific (e.g., `Sedan`, `SUV`, `Convertible`).
