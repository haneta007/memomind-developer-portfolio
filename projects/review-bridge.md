# Review Bridge

Review Bridge is a Windows and Android utility for continuing a code-review workflow away from the PC. On Windows, the user prepares a review package. On Android, the user shares it with a review app and sends the selected result back to the same job.

## Implementation

- A C#/.NET service manages packages and tracks job state. The Windows client uses WPF. The Android client is written in Kotlin.
- Pairing uses a time-limited code. The phone accesses job endpoints over HTTPS with a device credential.
- The transfer flow checks ZIP packages, tracks job status, and provides ways to handle failed or cancelled jobs.

## Evidence

The implementation separates job state, package validation, pairing, and the Android client. In an isolated checkout, all 104 core tests passed. I also inspected the existing API integration tests for missing credentials, expired pairing codes, device revocation, and the phone-side round trip. Physical-device validation was outside this check.

This project is the clearest example in my portfolio of coordinating state and handling failures across a phone and a second device.

[Selected projects](../PROJECTS.md)
