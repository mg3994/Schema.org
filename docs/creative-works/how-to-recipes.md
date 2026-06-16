# Recipes & How-To Documentation

Documentation for step-by-step instructions, whether for cooking or general tasks.

## Core Types

*   **Recipe**: A specific type of How-To for cooking.
*   **HowTo**: General instructions for any task.
*   **HowToStep**: An individual step in the process.
*   **HowToSection**: A group of related steps.
*   **HowToDirection**: A specific direction within a step.

---

## Comprehensive Example: Recipe (JSON-LD)

```json
{
  "@context": "https://schema.org/",
  "@type": "Recipe",
  "name": "Classic Sourdough Bread",
  "image": [
    "https://example.com/photos/1x1/photo.jpg",
    "https://example.com/photos/4x3/photo.jpg"
  ],
  "author": {
    "@type": "Person",
    "name": "Artisan Baker Jack"
  },
  "datePublished": "2025-03-10",
  "description": "A crusty, tangy sourdough loaf made with just flour, water, and salt.",
  "prepTime": "PT30M",
  "cookTime": "PT45M",
  "totalTime": "PT24H",
  "keywords": "sourdough, bread, baking, artisan",
  "recipeYield": "1 loaf",
  "recipeCategory": "Bread",
  "recipeCuisine": "International",
  "nutrition": {
    "@type": "NutritionInformation",
    "calories": "250 calories",
    "fatContent": "1 gram"
  },
  "recipeIngredient": [
    "500g Bread Flour",
    "350g Water",
    "100g Sourdough Starter",
    "10g Salt"
  ],
  "recipeInstructions": [
    {
      "@type": "HowToStep",
      "name": "Mix the dough",
      "text": "Combine flour and water and let rest for 1 hour.",
      "url": "https://example.com/recipe#step1",
      "image": "https://example.com/photos/step1.jpg"
    },
    {
      "@type": "HowToStep",
      "name": "Add starter and salt",
      "text": "Mix in your active starter and salt, kneading until smooth.",
      "url": "https://example.com/recipe#step2",
      "image": "https://example.com/photos/step2.jpg"
    }
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.9",
    "reviewCount": "512"
  },
  "video": {
    "@type": "VideoObject",
    "name": "How to Shape Sourdough",
    "description": "Learn the best technique for shaping your loaf.",
    "thumbnailUrl": "https://example.com/video-thumb.jpg",
    "contentUrl": "https://example.com/video.mp4",
    "uploadDate": "2025-03-10T12:00:00Z"
  }
}
```

## Tips for Recipes & How-Tos
*   **Step Images**: Include an image for every `HowToStep`. This makes the instructions much clearer for both users and search engines.
*   **Total Time**: Don't forget to include `prepTime`, `cookTime`, and `totalTime` in ISO 8601 duration format.
*   **Supply vs. Tool**: For general `HowTo`, use `supply` for consumable items and `tool` for non-consumable equipment.
*   **Video Integration**: A video showing the process significantly boosts engagement and rich result visibility.

## Things to Avoid
*   **Missing Steps**: Every recipe or guide must have at least one step.
*   **Vague Ingredients**: Be precise with measurements (e.g., "500g" instead of "some").
*   **Hidden Nutrition**: If you provide nutrition info, ensure it's visible on the page.
