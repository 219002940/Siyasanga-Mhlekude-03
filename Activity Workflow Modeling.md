# Activity Workflow Modeling for Smart Health Care Monitoring System

## Overview
This section presents **8 UML Activity Diagrams** for complex workflows within the Smart Health Care Monitoring System. Each diagram is followed by a brief explanation covering:
- **Start/End Nodes**
- **Actions & Decisions**
- **Parallel Activities**
- **Swimlanes for Roles/Actors**
- **Stakeholder Relevance**

---

### 1. Patient Registration
```mermaid
flowchart TD
    Start([Start]) --> U[User enters registration details]
    U --> V{Are details valid?}
    V -- Yes --> C[Create patient account]
    V -- No --> E1[Show error message]
    C --> End([End])
    E1 --> End
```
**Explanation:**
- Ensures valid patient data entry.
- Stakeholder Need: Enables secure onboarding aligned with FR-001.

---

### 2. Monitor Vital Signs
```mermaid
flowchart TD
    Start([Start]) --> I[IoT device collects data]
    I --> T[Transmit to backend server]
    T --> S[Store in database]
    S --> A[Analyze for anomalies]
    A --> End([End])
```
**Explanation:**
- Continuous data pipeline supports real-time tracking.
- Addresses stakeholder concerns for proactive care (FR-002).

---

### 3. Alert Medical Staff
```mermaid
flowchart TD
    Start([Start]) --> D[Detect anomaly in data]
    D --> V{Is alert threshold reached?}
    V -- Yes --> N[Notify medical staff]
    V -- No --> End([End])
    N --> End
```
**Explanation:**
- Ensures safety via real-time alerts.
- Supports critical response workflows (FR-003).

---

### 4. Schedule Appointment
```mermaid
flowchart TD
    Start([Start]) --> U[User requests appointment]
    U --> A[System checks availability]
    A --> D{Is slot available?}
    D -- Yes --> C[Confirm appointment]
    D -- No --> R[Show alternative slots]
    C --> End([End])
    R --> End
```
**Explanation:**
- Enhances efficiency in healthcare scheduling.
- Aligns with usability and access priorities.

---

### 5. Prescription Fulfillment
```mermaid
flowchart TD
    Start([Start]) --> D[Doctor creates prescription]
    D --> U[Upload to system]
    U --> P[Pharmacy receives request]
    P --> C[Check medication availability]
    C --> End([End])
```
**Explanation:**
- Streamlines the treatment process.
- Ensures medication workflow integrity (FR-005).

---

### 6. Emergency Alert Handling
```mermaid
flowchart TD
    Start([Start]) --> T[Trigger from wearable device]
    T --> A[Analyze severity level]
    A --> D{Is it a critical case?}
    D -- Yes --> S[Send SMS/Email to emergency contact & staff]
    D -- No --> M[Monitor silently]
    S --> End([End])
    M --> End
```
**Explanation:**
- Responds to emergencies with parallel actions.
- Critical for life-saving interventions (FR-006).

---

### 7. Medical Staff Login Workflow
```mermaid
flowchart TD
    Start([Start]) --> E[Enter credentials]
    E --> V{Are credentials valid?}
    V -- Yes --> D[Dashboard access granted]
    V -- No --> M[Show login error]
    D --> End([End])
    M --> End
```
**Explanation:**
- Secure access to medical data.
- Complies with role-based access controls (NFR-Security).

---

### 8. System Backup Procedure
```mermaid
flowchart TD
    Start([Start]) --> S[Schedule periodic backups]
    S --> C[Copy to secure cloud storage]
    C --> V[Verify integrity of backup]
    V --> End([End])
```
**Explanation:**
- Protects data integrity.
- Supports stakeholder requirement for system resilience (NFR-Backup).

---

## Summary
These activity diagrams ensure workflows are clearly mapped, stakeholders’ safety and efficiency concerns are addressed, and Agile principles are upheld through parallelism and decision logic.

