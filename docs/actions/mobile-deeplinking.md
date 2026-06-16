# Mobile & Deep Linking in Actions

Modern Schema.org implementation focuses on helping users take action across devices. This is achieved through `EntryPoint` and `PotentialAction` properties.

## Core Properties

*   **EntryPoint**: How to access a service or content.
*   **urlTemplate**: The URL with optional placeholders (e.g., `https://app.example.com/item/{id}`).
*   **actionPlatform**: The platform where the action is available (DesktopWeb, MobileWeb, Android, iOS).
*   **appSize / appVersion**: Metadata for the mobile application.

---

## Comprehensive Example: In-App Potential Action (JSON-LD)

This example shows how to document an action that opens directly in a mobile app (iOS or Android) if installed, or falls back to the web.

```json
{
  "@context": "https://schema.org",
  "@type": "Movie",
  "name": "The Great Adventure",
  "potentialAction": {
    "@type": "WatchAction",
    "target": [
      {
        "@type": "EntryPoint",
        "urlTemplate": "https://www.example.com/movies/123",
        "actionPlatform": "http://schema.org/DesktopWebPlatform"
      },
      {
        "@type": "EntryPoint",
        "urlTemplate": "example-app://movies/123",
        "actionPlatform": "http://schema.org/IOSPlatform"
      },
      {
        "@type": "EntryPoint",
        "urlTemplate": "intent://movies/123#Intent;scheme=example-app;package=com.example.app;end",
        "actionPlatform": "http://schema.org/AndroidPlatform"
      }
    ]
  }
}
```

## Tips for Deep Linking
*   **Multiple EntryPoints**: Provide an array of `EntryPoint` objects to cover all platforms.
*   **URL Schemes**: Use custom URL schemes for iOS (`myapp://`) and Intents for Android.
*   **Universal Links**: If you support Universal Links (iOS) or App Links (Android), the `urlTemplate` can be a standard HTTPS URL.
*   **Action Status**: Use `PotentialActionStatus` to indicate that the user *could* perform this action.

## Things to Avoid
*   **Broken Schemes**: Ensure the custom URL schemes match what's defined in your app's manifest.
*   **Missing Web Fallback**: Always provide a `DesktopWebPlatform` entry point for users without the app.
*   **Generic Targets**: Don't just point to the app's home screen; point to the specific content or action page.
