# Test Case Development for Smart Healthcare Monitoring System

## Functional Test Cases

| Test Case ID | Requirement ID | Description | Steps | Expected Result | Actual Result | Status |
|-------------|---------------|-------------|-------|----------------|--------------|--------|
| TC-001 | FR-001 | Collect patient vitals from IoT sensors | 1. Connect IoT device. 2. Start data collection. | System receives vitals and stores them in the database. | TBD | TBD |
| TC-002 | FR-002 | Process vitals in real-time | 1. Send vitals from IoT device. 2. System processes data. | Processing time <1 second. | TBD | TBD |
| TC-003 | FR-003 | Trigger alert for abnormal vitals | 1. Enter abnormal vitals. 2. System analyzes data. | Alert is generated within 2 seconds. | TBD | TBD |
| TC-004 | FR-004 | View patient dashboard | 1. Doctor logs in. 2. Selects patient. | Dashboard displays latest vitals. | TBD | TBD |
| TC-005 | FR-005 | Acknowledge and dismiss alerts | 1. Doctor views alert. 2. Clicks acknowledge. | Alert is marked as resolved. | TBD | TBD |
| TC-006 | FR-006 | Store patient vitals securely | 1. Capture vitals. 2. Store in database. | Data stored with AES-256 encryption. | TBD | TBD |
| TC-007 | FR-007 | Integrate with hospital systems | 1. Request patient data via API. | API responds with correct data format. | TBD | TBD |
| TC-008 | FR-010 | Generate patient health reports | 1. Doctor requests report. 2. System compiles data. | Downloadable PDF/CSV report is generated. | TBD | TBD |

## Non-Functional Test Cases

| Test Case ID | Requirement ID | Description | Test Scenario | Expected Result | Actual Result | Status |
|-------------|---------------|-------------|--------------|----------------|--------------|--------|
| TC-009 | NFR-001 | System Performance | Monitor system response time for 10,000 concurrent users. | System remains stable and responsive. | TBD | TBD |
| TC-010 | NFR-002 | Data Security | Attempt unauthorized access. | System denies access and logs attempt. | TBD | TBD |

This document ensures robust validation of functional and non-functional requirements for the **Smart Healthcare Monitoring System**. 🚀
