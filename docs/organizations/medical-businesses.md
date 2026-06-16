# Healthcare & Medical Businesses

Documentation for local healthcare providers, clinics, and pharmacies.

## Core Types

*   **MedicalClinic**: A facility providing medical services.
*   **Pharmacy**: A business where drugs are dispensed.
*   **Physician**: A medical doctor.
*   **IndividualPhysician**: A specific person who is a physician.
*   **Optician / Dentist / Dermatology**: Specialized medical practices.
*   **Hospital**: A large healthcare institution providing treatment.

---

## Comprehensive Example: Medical Clinic (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalClinic",
  "name": "Springfield Health Center",
  "image": "https://example.com/clinic.jpg",
  "telephone": "+15550004444",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "456 Wellness Way",
    "addressLocality": "Springfield",
    "addressRegion": "IL"
  },
  "medicalSpecialty": "https://schema.org/PrimaryCare",
  "availableService": [
    { "@type": "MedicalProcedure", "name": "Annual Physical Exam" },
    { "@type": "MedicalTest", "name": "Blood Pressure Screening" }
  ],
  "healthcareReportingData": {
    "@type": "CDCPMDRecord",
    "datePosted": "2025-01-01"
  }
}
```

## Tips for Medical Businesses
*   **Specialty**: Always use the `medicalSpecialty` property with valid Schema.org URLs (e.g., `https://schema.org/Pediatric`).
*   **Insurance**: Use `healthPlanNetworkId` if you want to indicate which insurance plans you accept (though this property is highly specialized).
*   **Services**: List common procedures and tests using `availableService`.
*   **Credentials**: Link to individual physicians using the `employee` or `founder` properties.

## Things to Avoid
*   **Missing Specialty**: Patients search by specialty (e.g., "Dentist"); ensuring this is marked up is vital.
*   **Generic Images**: Use photos of your actual facility to build patient trust.
*   **Non-standard Hours**: Clinics often have complex hours; use `openingHoursSpecification` for clarity.
