## 2. Functional Requirements

| ID | Requirement | Acceptance Criteria |
|----|------------|--------------------|
| FR1 | The system shall collect patient vitals from IoT devices | Data is received and stored in the database without loss |
| FR2 | The system shall process vitals in real-time | Latency for processing must be <1 second |
| FR3 | The system shall trigger alerts when abnormal vitals are detected | Alerts must be sent within 2 seconds of detection |
| FR4 | The system shall provide a dashboard for medical staff to view patient vitals | Data should be accessible via a web and mobile app |
| FR5 | The system shall allow doctors to acknowledge and dismiss alerts | Status updates should reflect in real-time |
| FR6 | The system shall store patient vitals securely in a database | Data encryption must follow AES-256 standards |
| FR7 | The system shall integrate with existing hospital management systems | API endpoints should be available for data sharing |
| FR8 | The system shall support access control based on user roles | Unauthorized users should not be able to access patient data |
| FR9 | The system shall provide historical data for analysis | Medical staff can access patient history for trends |
| FR10 | The system shall generate automated reports on patient health trends | Reports should be downloadable in PDF/CSV formats |
