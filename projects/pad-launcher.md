# Pad Launcher

Pad Launcher is a Kotlin and Jetpack Compose Android home app. It combines a launcher interface with an inbox for collecting items to review later, including items received through Android sharing.

## Implementation

- The manifest registers a home activity, and the launcher UI brings app actions and inbox entries into one interface.
- The inbox and AI triage are implemented as separate parts of the app. An OpenAI provider handles requests and parses responses for inbox review features.
- The Review Bridge integration uses a signature-protected Android permission for data exchange between the apps.

## Evidence

The Android manifest, inbox flow, AI provider, and app-to-app contract show how the features connect. Existing tests cover AI response parsing and inbox-review behavior. These are source-level examples of work on Android UI, AI service integration, and permission boundaries.

[Selected projects](../PROJECTS.md)
