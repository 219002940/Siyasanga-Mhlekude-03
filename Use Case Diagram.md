Key Actors & Roles
Patient – Provides real-time health data through IoT devices.
Doctor/Nurse – Monitors patient vitals, acknowledges alerts, and makes medical decisions.
IoT Sensors – Collect patient vitals and send data to the backend.
Hospital IT Staff – Ensures system functionality, performs maintenance, and secures data.
Hospital Administrator – Manages staff access and oversees compliance.
Family Members – Requests patient condition updates with authorized access.
Regulatory Bodies – Ensures compliance with healthcare data standards and audits system reports.
Relationships & Use Case Descriptions
Generalization: The Doctor/Nurse and Family Member both interact with View Patient Dashboard, but Family Members have limited access.
Inclusion:
"Acknowledge Alerts" includes "View Patient Dashboard" since doctors must check data before responding.
"Generate Compliance Reports" includes "View Patient History" to track medical trends.
Addressing Stakeholder Concerns
This diagram aligns with Assignment 4 stakeholder needs: ✅ Patients – Ensures real-time health tracking.
✅ Doctors/Nurses – Provides quick access to patient vitals and AI alerts.
✅ Hospital IT Staff – Maintains system uptime and data security.
✅ Hospital Administrators – Manages user roles and access.
✅ Family Members – Can access patient information securely.
✅ Regulators – Can audit system compliance and generate reports.
```mermaid
graph TD
    subgraph "Smart Healthcare Monitoring System"
        Patient["🧑 Patient"] --|Provides Vital Signs|--> IoT_Device["📟 IoT Sensors"]
        Doctor["👨‍⚕️ Doctor/Nurse"] --|Monitors Patient Data|--> Dashboard["📊 View Patient Dashboard"]
        Doctor --|Acknowledges Alerts|--> Alert_System["🚨 AI Alert System"]
        IT_Staff["💻 Hospital IT Staff"] --|Maintains System|--> System_Admin["⚙️ System Configuration"]
        Admin["🏥 Hospital Administrator"] --|Manages User Roles|--> System_Admin
        Family["👨‍👩‍👧 Family Member"] --|Requests Patient Updates|--> Patient_Info["📄 View Patient History"]
        Regulator["🏛️ Government/Regulatory Body"] --|Audits System Compliance|--> Compliance_Report["📜 Generate Compliance Reports"]

        IoT_Device --|Sends Data|--> Backend["🖥️ Python Backend"]
        Backend --|Stores & Processes|--> Database["🗄️ Secure Database"]
        Alert_System --|Triggers Notifications|--> Doctor
        System_Admin --|Manages Access|--> Dashboard
    end

