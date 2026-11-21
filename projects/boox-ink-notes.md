# BOOX Ink Notes

BOOX Ink Notes is an Android notebook for handwriting on E Ink devices. It captures stylus input, renders strokes in a canvas, and saves notes for later editing.

## Implementation

- A custom Android canvas and live-ink overlay handle handwriting. Stroke data includes coordinates and pressure.
- The note model and repository preserve the handwritten content when a note is saved and reopened.
- The E Ink controller separates display-specific behavior from the notebook UI, which lets the app handle capabilities that depend on the device.

## Evidence

The canvas, ink model, note repository, and display controller support these claims. I describe the implemented features here. Display latency and refresh behavior depend on the hardware.

My interest in MemoMind One follows a similar design question. How much information is useful on a display whose constraints differ from a phone screen?

[Selected projects](../PROJECTS.md)
