# Create & Update Actions

Documentation for actions involving the creation of new things or updating existing ones.

## Core Types

### Creation
*   **CreateAction**: The base for creation.
*   **CookAction**: Cooking food.
*   **DrawAction**: Drawing an image.
*   **FilmAction**: Filming a video.
*   **PaintAction**: Painting a picture.
*   **PhotographAction**: Taking a photo.
*   **WriteAction**: Writing text.

### Updates
*   **UpdateAction**: The base for updates.
*   **AddAction**: Adding a part to a whole.
*   **InsertAction**: Inserting an item.
*   **AppendAction / PrependAction**: Specific types of insertion.
*   **DeleteAction**: Removing an item.
*   **ReplaceAction**: Replacing one item with another.

---

## Comprehensive Example: WriteAction (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "WriteAction",
  "agent": {
    "@type": "Person",
    "name": "Jane Austen"
  },
  "object": {
    "@type": "Book",
    "name": "Pride and Prejudice"
  },
  "language": "English",
  "instrument": {
    "@type": "Thing",
    "name": "Pen and Paper"
  }
}
```

## Tips for Creation Actions
*   **Instrument**: Use the `instrument` property to describe the tools used (e.g., "Camera", "Adobe Photoshop").
*   **Result**: The `result` property should point to the created `CreativeWork`.
*   **Language**: For writing and speaking actions, specify the `language`.

## Things to Avoid
*   **Missing Creator**: Creation actions are useless without an `agent`.
*   **Generic Types**: Use `CookAction` or `WriteAction` instead of just `CreateAction`.
