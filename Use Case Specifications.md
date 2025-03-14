# Use Case Specifications for Smart Healthcare Monitoring System

## 1. Collect Patient Vitals
**Description:** The system collects real-time patient vitals from IoT sensors.
**Preconditions:** Patient is connected to the IoT device.
**Postconditions:** Vitals are stored in the database.
**Basic Flow:**
1. IoT device collects heart rate, blood pressure, and oxygen levels.
2. Data is transmitted to the backend.
3. Backend stores the data in the secure database.
**Alternative Flows:**
- IoT device fails to send data → Retry mechanism is triggered.

---

## 2. Monitor Patient Data
**Description:** Doctors and nurses view patient vitals in real-time.
**Preconditions:** Patient data is available in the system.
**Postconditions:** Medical staff can analyze patient vitals.
**Basic Flow:**
1. Doctor logs into the system.
2. Doctor selects a patient.
3. System displays the latest vitals.
**Alternative Flows:**
- No data available → System shows “No vitals recorded.”

---

## 3. Trigger Alerts for Abnormal Vitals
**Description:** The AI system triggers alerts when vitals are outside safe thresholds.
**Preconditions:** Vitals must be processed and analyzed.
**Postconditions:** Medical staff is notified.
**Basic Flow:**
1. System analyzes vitals.
2. AI detects abnormal patterns.
3. System sends an alert to the doctor.
**Alternative Flows:**
- False positive alert → Doctor dismisses the alert.

---

## 4. Acknowledge and Dismiss Alerts
**Description:** Doctors acknowledge and dismiss alerts once reviewed.
**Preconditions:** An alert must be generated.
**Postconditions:** Alert is marked as resolved.
**Basic Flow:**
1. Doctor logs into the system.
2. Doctor views pending alerts.
3. Doctor acknowledges the alert.
**Alternative Flows:**
- Doctor does not respond → System escalates the alert.

---

## 5. View Patient History
**Description:** Medical staff accesses historical patient data.
**Preconditions:** Patient must have previous vitals recorded.
**Postconditions:** Doctor can analyze trends.
**Basic Flow:**
1. Doctor logs in.
2. Doctor selects a patient.
3. System retrieves and displays past vitals.
**Alternative Flows:**
- No history found → System notifies doctor.

---

## 6. Manage User Access
**Description:** Administrators manage roles and permissions.
**Preconditions:** Admin has login credentials.
**Postconditions:** Users have correct access levels.
**Basic Flow:**
1. Admin logs in.
2. Admin selects a user.
3. Admin assigns or modifies roles.
**Alternative Flows:**
- Unauthorized modification attempt → System denies access.

---

## 7. Generate Compliance Reports
**Description:** Regulatory bodies generate system compliance reports.
**Preconditions:** System has stored patient data and logs.
**Postconditions:** Reports are available for review.
**Basic Flow:**
1. Regulator logs in.
2. Regulator selects “Generate Report.”
3. System compiles and exports data.
**Alternative Flows:**
- No data available → System notifies regulator.

---

## 8. Request Patient Updates (Family Members)
**Description:** Family members request patient health updates.
**Preconditions:** The patient must grant access.
**Postconditions:** Family receives authorized updates.
**Basic Flow:**
1. Family member logs in.
2. System verifies access rights.
3. System displays latest patient vitals.
**Alternative Flows:**
- Access denied → System notifies family member.

---

This document outlines key system functionalities, ensuring alignment with stakeholder needs and system requirements. 🚀
