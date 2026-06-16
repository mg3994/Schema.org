# Broadcasting & Media Channels

Documentation for describing television and radio stations, channels, and their technical specifications.

## Core Types

*   **BroadcastService**: A service that delivers content via a broadcast signal.
*   **BroadcastChannel**: A specific channel within a broadcast service.
*   **AMRadioChannel / FMRadioChannel**: Specific radio channel types.
*   **TelevisionChannel**: A specific television channel.
*   **BroadcastFrequencySpecification**: Technical details about the signal.

---

## Comprehensive Example: Television Station with Channels (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "BroadcastService",
  "name": "Global News Network",
  "broadcastDisplayName": "GNN",
  "videoFormat": "HD",
  "hasBroadcastChannel": [
    {
      "@type": "TelevisionChannel",
      "broadcastChannelId": "GNN-101",
      "broadcastServiceTier": "Standard",
      "genre": "News",
      "providesBroadcastService": { "@id": "https://example.com/gnn-service" }
    }
  ],
  "parentService": {
    "@type": "Organization",
    "name": "Global Media Group"
  }
}
```

## Comprehensive Example: Radio Station Frequency (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "FMRadioChannel",
  "name": "K-ROCK 98.1",
  "broadcastFrequency": {
    "@type": "BroadcastFrequencySpecification",
    "broadcastFrequencyValue": "98.1",
    "broadcastSignalModulation": "FM"
  },
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Los Angeles",
    "addressRegion": "CA"
  }
}
```

## Tips for Broadcasting
*   **Call Signs**: Use the `name` or `alternateName` to specify FCC or local call signs (e.g., "KROQ").
*   **Frequency**: Be precise with the `broadcastFrequencyValue` for radio stations.
*   **Coverage**: Use `areaServed` to show the geographic reach of the broadcast signal.
*   **Programs**: Link to `PodcastSeries` or `TVSeries` broadcast on the channel.

## Things to Avoid
*   **Confusing Service with Channel**: A `BroadcastService` is the provider, while a `BroadcastChannel` is the specific dial/frequency.
*   **Missing Modulation**: Always specify if it's AM or FM for radio.
