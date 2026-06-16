# Job Postings Schema Documentation

Documentation for describing specific job openings at an organization.

## Core Properties

*   **title**: The name of the position.
*   **hiringOrganization**: The organization offering the job.
*   **jobLocation**: The physical location(s) of the job.
*   **baseSalary**: The salary range for the position.
*   **employmentType**: Full-time, part-time, contract, etc.
*   **datePosted**: When the job was listed.
*   **validThrough**: When the job listing expires.
*   **applicantLocationRequirements**: For remote jobs, where the applicant must live.
*   **jobLocationType**: Use `TELECOMMUTE` for fully remote jobs.

---

## Comprehensive Example: Remote Senior Developer (JSON-LD)

```json
{
  "@context": "https://schema.org/",
  "@type": "JobPosting",
  "title": "Senior Frontend Engineer (Remote)",
  "description": "<p>We are seeking an expert in React and TypeScript to join our globally distributed team.</p>",
  "identifier": {
    "@type": "PropertyValue",
    "name": "TechFlow",
    "value": "FE-SR-2025"
  },
  "datePosted": "2025-05-01",
  "validThrough": "2025-08-01",
  "employmentType": "FULL_TIME",
  "hiringOrganization": {
    "@type": "Organization",
    "name": "TechFlow Systems",
    "sameAs": "https://www.techflow.systems",
    "logo": "https://www.techflow.systems/logo.png"
  },
  "jobLocationType": "TELECOMMUTE",
  "applicantLocationRequirements": {
    "@type": "Country",
    "name": "USA"
  },
  "baseSalary": {
    "@type": "MonetaryAmount",
    "currency": "USD",
    "value": {
      "@type": "QuantitativeValue",
      "minValue": 140000,
      "maxValue": 180000,
      "unitText": "YEAR"
    }
  },
  "experienceRequirements": {
    "@type": "OccupationalExperienceRequirements",
    "monthsOfExperience": 60
  }
}
```

## Tips for Job Postings
*   **Remote Jobs**: Always include `jobLocationType: TELECOMMUTE` and specify `applicantLocationRequirements` to help job seekers find remote roles.
*   **Salary Ranges**: Using `minValue` and `maxValue` in `baseSalary` is highly recommended for transparency and search visibility.
*   **Expiration**: Use `validThrough` to ensure search engines automatically remove the listing once it's filled.
*   **HTML in Description**: You can use basic HTML tags (like `<p>`, `<ul>`, `<li>`) in the `description` for better formatting.

## Things to Avoid
*   **Missing Organization**: A job must always be tied to a `hiringOrganization`.
*   **Generic Titles**: Use specific job titles (e.g., "Senior Java Developer" instead of "Developer").
*   **Keeping Expired Jobs**: Remove or update schema for jobs that are no longer accepting applications.
