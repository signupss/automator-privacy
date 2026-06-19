# Privacy Policy — Automator
Last updated: June 2026

## 1. What This App Does
Automator is an advanced, comprehensive macro engine and automation platform that allows users to build, execute, and manage fully customized workflow sequences on their Android devices. The app replaces dozens of single-purpose utility tools by integrating system gestures, hardware triggers, and cross-app workflows into a consolidated, zero-root automation ecosystem.

## 2. Absolute Data Privacy & Local Execution
We enforce a strict offline-first architecture. **We do not collect, store, upload, or share any personal data, usage metrics, or system information.**
* All configurations, automation scripts, logs, variables, and database records reside exclusively within the application's secure local storage on your device.
* No data ever leaves your device unless you explicitly configure an automation step to transmit a specific payload (e.g., via a custom HTTP request designed by you).

## 3. High-Risk & Sensitive Permissions Disclosures
To provide cross-app automation and execution of user-defined workflows, the app requires access to several sensitive Android frameworks. Every permission is utilized strictly in real-time to execute your explicit instructions.

### Accessibility Service API
Automator utilizes the `AccessibilityService` API to programmatically interact with the device UI. This includes:
* Simulating user inputs (taps, swipes, scrolls, and text typing).
* Reading screen content and UI element properties to detect specific text or image triggers.
* Monitoring window state changes to automate actions inside third-party apps.
This framework operates solely when a macro is running and does not log keystrokes, monitor active background behavior outside of macro rules, or capture credentials.

### File System & All Files Access (MANAGE_EXTERNAL_STORAGE)
The app uses file management permissions to store, load, export, and import macro files, script projects, and execution logs. It requires `MANAGE_EXTERNAL_STORAGE` to automate complex local file operations—such as automatic backups, project synchronization, directory pruning, and processing files of arbitrary extensions (.json, .xml, .cfg)—across user-accessible directories without disrupting background automation loops.

### Location Data & Geofencing (Fine, Coarse, and Background Location)
Location data is processed strictly in real-time and entirely offline. The app accesses location in the background solely to evaluate user-configured geofencing triggers (e.g., executing a macro when entering or leaving a specified geographic area). We do not track, map, or retain historical location logs.

### SMS & Telephony Automation
Automator contains modules for interacting with cellular features, which execute only if the device has physical telephony hardware:
* **SMS Permissions (SEND_SMS, READ_SMS, RECEIVE_SMS):** Used strictly to trigger macros upon receiving a specific SMS message, or to programmatically send automated notifications based on your rules.
* **Phone Permissions (CALL_PHONE, ANSWER_PHONE_CALLS, READ_PHONE_STATE):** Used to detect incoming/outgoing call states to act as macro triggers, or to automate hands-free call handling within your workflows.

### Personal Data: Contacts & Calendar
* **Contacts (READ_CONTACTS, WRITE_CONTACTS):** Accessed only to look up contact names or manage records when executing user-configured communication macros.
* **Calendar (READ_CALENDAR, WRITE_CALENDAR):** Used to check scheduled events as macro entry conditions or to automate the creation/modification of appointments.

### Package Visibility (QUERY_ALL_PACKAGES)
The app queries the list of installed applications on the device to populate macro configuration menus, allowing you to select target apps for launching, stopping background processes, or executing context-specific automated tasks.

### Notification Listener Service
The app monitors incoming system notifications purely to act as a trigger mechanism, allowing macros to fire automatically when specific text patterns or apps post a notification.

### Device Administration & Secure System Settings
* **Device Admin (BIND_DEVICE_ADMIN):** Used exclusively to invoke the system force-lock action when executing a screen-lock macro step.
* **System Settings (WRITE_SETTINGS, WRITE_SECURE_SETTINGS via Shizuku integration):** Used to automate system toggles (such as proxy setups, display behavior, or advanced system flags) exactly as defined in your macro steps.

## 4. Hardware and Connectivity Controls
The app accesses various hardware features purely to bridge them into automation workflows:
* **Camera & Microphone:** Used exclusively when executing macro steps that involve capturing photos (e.g., for visual recognition triggers) or recording temporary audio clips.
* **Hardware Sensors:** Reads accelerometer, gyroscope, light, and proximity sensors to serve as physical environmental macro triggers.
* **Bluetooth, Wi-Fi & NFC:** Used to scan for nearby devices, change connectivity states, or trigger macro loops when interacting with specific NFC tags or network environments.

## 5. Third-Party Services & AI Integrations
Automator does not include third-party analytics SDKs, advertising networks, or tracking frameworks. 
If you choose to use the AI Agent feature, text/visual prompts are sent directly to your designated API providers (such as OpenAI or Anthropic) via their official endpoints using API keys securely stored in your local encrypted storage. These interactions are governed entirely by the privacy policies of those respective providers.

## 6. Children's Privacy
This application is designed for developer and power-user automation utilities; it is not directed at children under the age of 13, and we do not knowingly interact with or collect data from minors.

## 7. Contact Information
For technical queries regarding local permission enforcement or this policy, please reach out to us at: support.logicnexus@gmail.com
