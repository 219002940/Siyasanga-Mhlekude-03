# 📦 Object State Modeling - Smart Health Care Monitoring System

This section outlines 8 critical system objects with their respective UML state transition diagrams using Mermaid, along with an explanation of key states and how each diagram aligns with functional requirements.

---

## 1. 👤 Patient
```mermaid
stateDiagram-v2
    [*] --> Registered
    Registered --> Active : Patient Verified
    Active --> Discharged : Treatment Complete
    Active --> Inactive : No Activity for 30 Days
    Inactive --> Active : Reactivation
    Discharged --> [*]
```
**Explanation:**
- **Key States:** Registered, Active, Inactive, Discharged
- **Transitions:** Based on verification, inactivity, or treatment completion.
- **Mapping:** Aligns with FR-001: Register and manage patient profiles.

---

## 2. 📶 SensorDevice
```mermaid
stateDiagram-v2
    [*] --> Initialized
    Initialized --> Monitoring : Connection Established
    Monitoring --> Faulty : Data Error Detected
    Faulty --> Maintenance : Diagnosis Initiated
    Maintenance --> Monitoring : Restored
    Monitoring --> [*] : Device Shutdown
```
**Explanation:**
- **Key States:** Initialized, Monitoring, Faulty, Maintenance
- **Mapping:** Addresses FR-004: Monitor patient vitals in real-time.

---

## 3. 🧪 SensorData
```mermaid
stateDiagram-v2
    [*] --> Captured
    Captured --> Validated : Format Verified
    Validated --> Stored : Added to Database
    Captured --> Discarded : Invalid Format
```
**Explanation:**
- **Key States:** Captured, Validated, Stored, Discarded
- **Mapping:** FR-006: Validate and store patient data securely.

---

## 4. 🚨 Alert
```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Triggered : Abnormal Vitals Detected
    Triggered --> Notified : Notify Medical Staff
    Notified --> Acknowledged : Staff Response Received
    Acknowledged --> Resolved : Patient Stabilized
    Resolved --> Idle
```
**Explanation:**
- **Key States:** Idle, Triggered, Notified, Acknowledged, Resolved
- **Mapping:** FR-008: Send alerts based on health thresholds.

---

## 5. 💬 Message
```mermaid
stateDiagram-v2
    [*] --> Composed
    Composed --> Sent : Submit
    Sent --> Delivered : Recipient Available
    Delivered --> Read : Opened by User
    Delivered --> Failed : Timeout/Error
```
**Explanation:**
- **Key States:** Composed, Sent, Delivered, Read, Failed
- **Mapping:** FR-007: Support messaging between staff and patients.

---

## 6. 🩺 Appointment
```mermaid
stateDiagram-v2
    [*] --> Requested
    Requested --> Confirmed : Approved by Staff
    Confirmed --> Completed : Session Held
    Requested --> Canceled : User Cancels
    Confirmed --> NoShow : Patient Missed
```
**Explanation:**
- **Key States:** Requested, Confirmed, Completed, Canceled, NoShow
- **Mapping:** FR-005: Allow users to book and cancel appointments.

---

## 7. 🧑‍⚕️ Medical Staff Account
```mermaid
stateDiagram-v2
    [*] --> Created
    Created --> Verified : Email Confirmed
    Verified --> Active : Admin Approval
    Active --> Suspended : Policy Violation
    Suspended --> Reactivated : Review Passed
```
**Explanation:**
- **Key States:** Created, Verified, Active, Suspended, Reactivated
- **Mapping:** FR-002: Manage staff credentials securely.

---

## 8. 🔒 User Session
```mermaid
stateDiagram-v2
    [*] --> Initiated
    Initiated --> Authenticated : Valid Credentials
    Authenticated --> Expired : Timeout
    Expired --> Terminated : Auto-Logout
    Authenticated --> Terminated : Manual Logout
```
**Explanation:**
- **Key States:** Initiated, Authenticated, Expired, Terminated
- **Mapping:** FR-009: Maintain secure user session.

---


