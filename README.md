# Thermal Monitor Support & Security Disclosure

## Technical Support & Contact
If you have security questions, encounter bugs, or need help with the app, please open a public ticket here:
👉 [Click Here to Contact Support]( https://github.com/EssumiShannag/thermal-monitor-info/issues)

---

## Why This App Requires Administrator Privileges
This  Windows Forms application is a lightweight thermal monitor designed to display three basic pieces of data on your desktop: CPU Package Temperature, CPU Load, and CPU Clock Speed. 

To provide accurate hardware monitoring on Windows, the application requires administrative elevation (`requireAdministrator`) for the following technical reasons:

* **Low-Level Hardware Access:** Windows security architecture restricts standard user accounts from accessing Model-Specific Registers (MSR) and motherboard sensor ICs where raw temperature data is stored. Administrative access is required to read these values.
* **Hardware Polling:** The app safely reads performance diagnostic data directly from the CPU hardware layer without altering any of your operating system configurations.

### Security Guarantees
* **Read-Only Operation:** The app operates strictly in a read-only capacity regarding hardware metrics. It does not modify system settings, registry hives, or files.
* **Privacy Safe:** The application does not collect, store, or transmit any personal data.
