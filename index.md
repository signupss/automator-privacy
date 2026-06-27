# Privacy Policy — Automator

**Last updated:** June 2026

---

## 1. What This App Does
Automator is an advanced, comprehensive macro engine and automation platform that allows users to build, execute, and manage fully customized workflow sequences on their Android devices. The app replaces dozens of single-purpose utility tools by integrating system gestures, hardware triggers, and cross-app workflows into a consolidated, zero-root automation ecosystem.

---

## 2. Absolute Data Privacy & Local Execution
We enforce a strict offline-first architecture. We do not collect, store, upload, or share any personal data, usage metrics, or system information.

All configurations, automation scripts, logs, variables, and database records reside exclusively within the application's secure local storage on your device.

No data ever leaves your device unless you explicitly configure an automation step to transmit a specific payload (e.g., via a custom HTTP request designed by you).

---

## 3. High-Risk & Sensitive Permissions Disclosures
To provide cross-app automation and execution of user-defined workflows, the app requires access to several sensitive Android frameworks. Every permission is utilized strictly in real-time to execute your explicit instructions.

### Accessibility Service API
Automator utilizes the `AccessibilityService` API to programmatically interact with the device UI. This includes:
* **Simulating user inputs** (taps, swipes, scrolls, and text typing) based strictly on user-defined macro steps.
* **Reading screen content** and UI element properties locally to detect specific text or image triggers.
* **Monitoring window state changes** to automate tasks inside apps as explicitly configured by the user.

> This framework operates solely when a macro is running and does not log keystrokes, monitor active background behavior outside of active macro rules, or capture credentials.

### Secure File Storage & Storage Access Framework (SAF)
Automator complies with modern Android scoped-privacy standards. The app **does not request or declare broad file system access permissions** (such as `MANAGE_EXTERNAL_STORAGE` or `READ_EXTERNAL_STORAGE`). Instead, data access is strictly sandboxed and user-controlled:
* **Storage Access Framework (SAF):** The app accesses external files or directories (such as `.json` or `.zip` macro packages) strictly through standard system intents (`ACTION_OPEN_DOCUMENT_TREE`, `ACTION_OPEN_DOCUMENT`). Persistent access is maintained entirely locally using secure, user-authorized URI permissions (`takePersistableUriPermission`).
* **Android Photo Picker:** Media resources required for visual automation triggers are selected securely via the native system Photo Picker, ensuring the app never reads or scans your wider photo library.
* **App-Scoped Local Storage:** Project assets, logs, and configuration databases are isolated entirely within the application’s private secure directories (`filesDir` / `getExternalFilesDir`), meaning they are entirely inaccessible to other applications.

### Location Data & Geofencing (Fine, Coarse, and Background Location)
Location data is processed strictly in real-time and entirely offline. The app accesses location in the background solely to evaluate user-configured geofencing triggers (e.g., executing a macro when entering or leaving a specified geographic area). We do not track, map, or retain historical location logs.

### SMS & Telephony Automation
Automator contains modules for interacting with cellular features, which execute only if the device has physical telephony hardware:
* **SMS Permissions (`SEND_SMS`, `READ_SMS`, `RECEIVE_SMS`):** Used strictly to trigger macros upon receiving a specific SMS message, or to programmatically send automated notifications based on your rules.
* **Phone Permissions (`CALL_PHONE`, `ANSWER_PHONE_CALLS`, `READ_PHONE_STATE`):** Used to detect incoming/outgoing call states to act as macro triggers, or to automate hands-free call handling within your workflows.

### Personal Data: Contacts & Calendar
* **Contacts (`READ_CONTACTS`, `WRITE_CONTACTS`):** Accessed only to look up contact names or manage records when executing user-configured communication macros.
* **Calendar (`READ_CALENDAR`, `WRITE_CALENDAR`):** Used to check scheduled events as macro entry conditions or to automate the creation/modification of appointments.

### Package Visibility & Application Management (QUERY_ALL_PACKAGES)
* **Package Visibility:** The app queries the list of installed applications on the device (`QUERY_ALL_PACKAGES`) solely to populate user configuration menus, allowing you to select specific target apps for launching, automated context switching, or termination.
* **Package Installation Handling:** Utilizing standard system requests (`REQUEST_INSTALL_PACKAGES`, `REQUEST_DELETE_PACKAGES`), the app can bridge user-triggered automation steps to launch the native package installer or uninstaller dialogs, requiring manual verification by the user at runtime.

### Notification Listener Service
The app monitors incoming system notifications purely to act as a trigger mechanism, allowing macros to fire automatically when specific text patterns or apps post a notification.

### Device Administration & Secure System Settings
* **Device Admin (`BIND_DEVICE_ADMIN`):** Used exclusively to invoke the system force-lock action when executing a screen-lock macro step.
* **System Settings (`WRITE_SETTINGS`):** Used to automate basic system toggles (such as display behavior, brightness, or connectivity profiles) exactly as defined in your macro steps.

---

## 4. Hardware and Connectivity Controls
The app accesses various hardware features purely to bridge them into automation workflows:
* **Camera & Microphone:** Used exclusively when executing macro steps that involve capturing photos (e.g., for visual recognition triggers) or recording temporary audio clips.
* **Hardware Sensors:** Reads accelerometer, gyroscope, light, and proximity sensors to serve as physical environmental macro triggers.
* **Bluetooth, Wi-Fi & NFC:** Used to scan for nearby devices, change connectivity states, or trigger macro loops when interacting with specific NFC tags or network environments.

---

## 5. Third-Party Services & Local AI Integration
Automator does not include third-party analytics SDKs, advertising networks, or tracking frameworks. If you choose to utilize the optional Design-Time AI Assistant or Local Data Parsing features, text/visual prompts are sent directly to your designated API providers (such as OpenAI or Anthropic) via their official endpoints using API keys securely stored in your local encrypted storage. These interactions are user-initiated at design-time and are governed entirely by the privacy policies of those respective providers.

---

## 6. Children's Privacy
This application is designed for developer and power-user automation utilities; it is not directed at children under the age of 13, and we do not knowingly interact with or collect data from minors.

---

## 7. Contact Information
For technical queries regarding local permission enforcement or this policy, please reach out to us at: support.logicnexus@gmail.com
