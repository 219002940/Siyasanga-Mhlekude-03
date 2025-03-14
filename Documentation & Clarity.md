# Smart Healthcare Monitoring System
## Test and Use Case Document

## Introduction
This document consolidates the **use case specifications** and **test case development** for the **Smart Healthcare Monitoring System**, ensuring alignment with stakeholder needs and system requirements.

---

## Use Case Specifications

Collect Patient Vitals
Description: The system collects real-time patient vitals from IoT sensors.
Preconditions:
- Patient is connected to the IoT device.
Postconditions:
- Vitals are stored in the database.

Basic Flow:
1. IoT device collects heart rate, blood pressure, and oxygen levels.
2. Data is transmitted to the backend.
3. Backend stores the data securely.

Alternative Flows:
- IoT device fails to send data → Retry mechanism is triggered.
### Monitor Patient Data
Description: Doctors and nurses view patient vitals in real-time.

Preconditions:
- Patient data is available in the system.

Postconditions:
- Medical staff can analyze patient vitals.
Basic Flow:
1. Doctor logs into the system.
2. Doctor selects a patient.
3. System displays the latest vitals.

Alternative Flows:
- No data available → System shows “No vitals recorded.”

---

## Test Case Development

| Test Case ID | Requirement ID | Description | Steps | Expected Result | Actual Result | Status |
|-------------|---------------|-------------|-------|----------------|--------------|--------|
| TC-001 | FR-001 | Collect patient vitals from IoT sensors | 1. Connect IoT device. 2. Start data collection. | System receives vitals and stores them in the database. | TBD | TBD |
| TC-002 | FR-002 | Process vitals in real-time | 1. Send vitals from IoT device. 2. System processes data. | Processing time <1 second. | TBD | TBD |
| TC-003 | FR-003 | Trigger alert for abnormal vitals | 1. Enter abnormal vitals. 2. System analyzes data. | Alert is generated within 2 seconds. | TBD | TBD |
| TC-004 | FR-004 | View patient dashboard | 1. Doctor logs in. 2. Selects patient. | Dashboard displays latest vitals. | TBD | TBD |


---

## Alignment with Stakeholder Needs
This document ensures:
-Stakeholder concerns** are addressed with clear use cases.
-Functional & non-functional requirements** are validated through structured test cases.
-Consistency** with previously defined requirements and architecture.

