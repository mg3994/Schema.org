# Credentials & Certifications

Documentation for describing professional certifications, academic degrees, and institutional accreditations.

## Core Types

*   **EducationalOccupationalCredential**: A degree, diploma, or certificate.
*   **Certification**: A professional certification.
*   **CertificationStatusEnumeration**: Active, Inactive, etc.
*   **Permit**: A license or permit.

---

## Comprehensive Example: Professional Certification (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Certification",
  "name": "Certified Cloud Professional",
  "description": "Validation of expert-level cloud infrastructure management.",
  "issuer": {
    "@type": "Organization",
    "name": "Cloud Authority Global"
  },
  "credentialCategory": "Professional Certification",
  "validIn": {
    "@type": "Country",
    "name": "US"
  },
  "certificationStatus": "https://schema.org/CertificationActive",
  "image": "https://example.com/badges/cloud-pro.png",
  "url": "https://example.com/verify/12345"
}
```

## Tips for Credentials
*   **Issuers**: Always identify the `issuer` organization.
*   **Verification**: Include a `url` where the credential can be verified.
*   **Expiry**: If the certification expires, include that info in the `description` or using a `validThrough` date if available on the specific type.
*   **Competencies**: For educational credentials, use `competencyRequired` to describe the skills gained.

## Things to Avoid
*   **Unverified Claims**: Only mark up credentials that can be officially verified.
*   **Confusion with Courses**: A `Course` is the learning process; a `Credential` is the resulting award.
*   **Vague Categories**: Be specific about whether it's a `PhD`, `Master's`, `Certificate`, or `License`.
