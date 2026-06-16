# Sports Activity Locations

Documentation for physical locations dedicated to sports and physical exercise.

## Core Types

*   **SportsActivityLocation**: The base type for all sports venues.
*   **BowlingAlley**: A venue for bowling.
*   **ExerciseGym**: A fitness center or gym.
*   **GolfCourse**: A course for playing golf.
*   **HealthClub**: Often used interchangeably with gyms but can include spa facilities.
*   **PublicSwimmingPool**: A public pool.
*   **SkiResort**: A location for skiing and winter sports.
*   **SportsClub**: A private or member-based sports club.
*   **StadiumOrArena**: Large venues for professional sports.
*   **TennisComplex**: A venue for tennis.

---

## Comprehensive Example: Exercise Gym (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "ExerciseGym",
  "name": "Iron & Steam Fitness",
  "image": "https://example.com/gym-interior.jpg",
  "telephone": "+15558883333",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "100 Heavy Lift Road",
    "addressLocality": "Muscle City",
    "addressRegion": "CA"
  },
  "openingHours": "Mo-Fr 05:00-23:00, Sa-Su 07:00-21:00",
  "amenityFeature": [
    { "@type": "LocationFeatureSpecification", "name": "Free Weights", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "Sauna", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "Personal Training", "value": true }
  ],
  "priceRange": "$$"
}
```

## Tips for Sports Locations
*   **Amenities**: List specific equipment or facilities (Pool, Sauna, Yoga Studio) using `amenityFeature`.
*   **Membership**: Use `Offer` to describe membership plans and pricing.
*   **Classes**: Use the `event` property to list specific fitness classes (Yoga, HIIT, etc.).
*   **Location**: Ensure `geo` coordinates are included for better mapping.

## Things to Avoid
*   **Generic Naming**: Be specific about the type of facility.
*   **Outdated Class Schedules**: If you list classes, keep the `event` data fresh.
*   **Missing Phone Number**: Local gyms rely heavily on phone inquiries for memberships.
