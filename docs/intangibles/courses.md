# Courses & Educational Content

Documentation for describing educational courses and their specific instances.

## Core Types

*   **Course**: The definition of a course (the "work").
*   **CourseInstance**: A specific occurrence of a course (e.g., "Fall 2025 Semester").
*   **LearningResource**: A broader type for any resource used for learning.

## Core Properties

*   **courseCode**: The identifier for the course (e.g., `CS101`).
*   **coursePrerequisites**: What a student needs to know before taking the course.
*   **educationalLevel**: The academic level (e.g., `Beginner`, `Undergraduate`).
*   **provider**: The institution or person providing the course.

---

## Comprehensive Example: Online Certificate Course (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Course",
  "name": "Professional Data Science Certificate",
  "description": "Master data analysis, visualization, and machine learning.",
  "courseCode": "DS-CERT-01",
  "educationalLevel": "Intermediate",
  "provider": {
    "@type": "Organization",
    "name": "Data Academy",
    "sameAs": "https://www.dataacademy.edu"
  },
  "hasCourseInstance": [
    {
      "@type": "CourseInstance",
      "courseMode": "Online",
      "instructor": {
        "@type": "Person",
        "name": "Dr. Sarah Data"
      },
      "startDate": "2025-06-01",
      "endDate": "2025-09-01",
      "offers": {
        "@type": "Offer",
        "price": "299.00",
        "priceCurrency": "USD"
      }
    }
  ]
}
```

## Tips for Courses
*   **Course Mode**: Specify if the course is `Online`, `Blended`, or `OnSite`.
*   **Prerequisites**: Use `coursePrerequisites` to help students understand if they are ready for the course.
*   **Outcomes**: Use `educationalCredentialAwarded` to describe the certificate or degree the student will receive.
*   **Reviews**: Link `AggregateRating` to the course to show student satisfaction.

## Things to Avoid
*   **Confusing Course with Class**: A `Course` is the subject (e.g., Calculus), while a `CourseInstance` is the specific class time.
*   **Missing Providers**: Always identify who is teaching or providing the course.
