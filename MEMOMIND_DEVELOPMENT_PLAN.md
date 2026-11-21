# Personal AI Companion for Smart Glasses

I plan to build a MemoMind One companion that shows one useful piece of information at a time. The Android phone handles input and longer interactions. The glasses show a short message the wearer can read at a glance. This is a development proposal.

## Start with a message

**MVP 1.** Run the official Hello Web example with GM Web Bridge in MemoMind Plugin Studio. On Windows, use the complete development kit and Edge WebView2, import the kit root, and select Hello Web and its matching glasses bridge. Build a PhoneSDK Web plugin inside the MemoMind App. Use the documented display API to create a page, update its text, and close it. Test an empty input, wrapping, and connection loss with synthetic text. Success means that a phone-side action reliably changes a readable short message on the virtual glasses display. Repeat on MemoMind One once the compatible companion app, firmware, glasses, and developer workspace access are available. Record Studio and physical-device results independently. [Official Web plugin tutorial](https://open-platform.memo-mind.com/docs/get-started/quickstart/first-web-app/) · [Device testing](https://open-platform.memo-mind.com/docs/get-started/quickstart/lan-install/?lang=en)

**MVP 2.** Add a phone-side action that requests a short AI answer from a service I control. Keep service credentials on the server. Ask before transmitting the input, send only the necessary text, and show clear feedback for empty answers, timeouts, or a lost glasses connection. Start with synthetic requests and a simulated response. Success means that the requested response displays as a short, readable summary and the wearer can dismiss it. [MemoMind networking and AI integration](https://open-platform.memo-mind.com/docs/build/networking/?lang=en)

**MVP 3.** Show selected tasks and upcoming events. Begin with an in-app list or an explicitly chosen import so I can test relevance and legibility without broad access to phone data. Add user-selected Android notifications or calendar integration only after validating an authorized handoff from the phone. Keep private content hidden until the wearer chooses to open it.

## SDK capabilities and validation

| Status | Capability |
| --- | --- |
| Documented | Phone Web display and storage, network calls to a developer-operated service, and paired messages between phone and glasses plugins with declared permissions. |
| Documented with device prerequisites | Short audio capture and button or gesture events. Check host capabilities, permissions, and the input path on the physical device. |
| Requires investigation | Access to Android system notifications or calendars from a supported integration, reliable background delivery, and wake or reconnect behavior on the target phone and glasses. |
| Future work | On-demand voice input, transcription through a service, and more controls from the glasses. The documented PhoneSDK does not provide a general-purpose built-in language model or transcription service. |

[MemoMind platform capabilities](https://open-platform.memo-mind.com/docs/build/capabilities/?lang=en) · [Web SDK reference](https://open-platform.memo-mind.com/docs/build/web-sdk/?lang=en) · [Audio capture guide](https://open-platform.memo-mind.com/docs/build/web-audio/?lang=en)

[Portfolio home](README.md)
