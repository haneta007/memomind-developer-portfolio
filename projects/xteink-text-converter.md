# XTEINK Text Converter

XTEINK Text Converter is an Android tool for preparing documents for E Ink reading. It accepts plain text and PDFs that contain extractable text, gives the reader a preview, and exports a UTF-8 TXT file.

## Implementation

- A Kotlin conversion module detects chapter headings, cleans repeated headers and footers, and normalizes line breaks and paragraphs.
- The Android interface uses Jetpack Compose. The app uses Android PDF APIs to extract text. The conversion and export logic lives in a separate module.
- The preview lets the reader review how source text is transformed before exporting.

## Evidence

The input loader, conversion pipeline, preview, and exporter provide a traceable path from selecting a document to creating the output file. All 53 existing conversion-module tests passed when run directly with Kotlin and JUnit in an isolated folder. They cover plain-text extraction, chapter detection, conversion behavior, and TXT export. The Android PDF extraction path was reviewed in source.

[Selected projects](../PROJECTS.md)
