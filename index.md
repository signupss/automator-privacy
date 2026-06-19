# Privacy Policy — Automator
Last updated: June 2026

## What this app does
Automator is a macro automation tool that allows users to build and run automated sequences of actions on their Android device. It uses Android’s Accessibility Service to simulate taps, swipes, and other gestures, and to read text and UI elements visible on the screen.

## Data we collect
We collect no personal data. 
Automator does not collect, store, transmit, or share any information about you, your device, or your location with us or any third party. 
All macro configurations, variables, logs, and settings are stored locally on your device only. Nothing leaves your device.

## Location Data Usage
Automator accesses your device's location data (including background location, if configured for automated triggers) solely to enable location-based macro triggers and geofencing workflows that you explicitly build. This data is processed entirely in real-time and strictly offline on your device to determine if a macro should execute based on your geographic coordinates. We never store, track, or transmit your location data to any external servers.

## Accessibility Service
Automator uses Android’s AccessibilityService API to:
* Simulate user gestures (taps, swipes, scrolls, typing)
* Read text and UI element properties visible on the screen
* Detect when specific text or images appear on screen

This permission is used solely to execute the automation actions that you explicitly configure and trigger. The Accessibility Service does not log keystrokes, does not capture passwords or sensitive input, and does not monitor your activity in the background unless a macro is actively running.

## Permissions explained
* Accessibility Service — to simulate gestures and read UI elements
* Location (Fine/Coarse/Background) — strictly to trigger specific macros automatically based on your location or geofencing rules
* Display over other apps — to show overlay panels during macro runs
* Camera — only if you use camera-related macro actions
* Microphone — only if you use audio recording macro actions
* Internet — to make HTTP requests from within your macros (only when you explicitly add an HTTP step)
* Receive boot broadcast — to restore your scheduled macros after the device restarts

No permission is used for tracking, advertising, or analytics.

## Third-party services
Automator does not integrate any analytics SDKs, advertising networks, or crash reporting services that send data to external servers. 
If you use the AI Agent feature with an external API (such as OpenAI or Anthropic), your prompts are sent to that provider according to their own privacy policy. API keys are stored locally on your device in encrypted storage.

## Children
This app is not directed at children under 13 and we do not knowingly collect data from children.

## Changes
If this policy changes, we will update the date at the top of this page.

## Contact
If you have any questions about this privacy policy, contact us at: support.logicnexus@gmail.com
