# Assignment 9: Domain Modeling and Class Diagram Development

##Domain Model Documentation

The following table outlines key domain entities, their attributes, methods, relationships, and applicable business rules for the Smart Health Care Monitoring System.

| Entity         | Attributes                                         | Methods                                 | Relationships                            | Business Rules |
|----------------|----------------------------------------------------|-----------------------------------------|------------------------------------------|----------------|
| Patient        | patientId, name, age, gender, contactInfo         | register(), updateProfile()             | Assigned to Device, linked to Alerts     | A patient can have multiple devices. |
| Device         | deviceId, type, status, batteryLevel               | sendData(), checkStatus()               | Belongs to Patient                        | Devices must be assigned to patients. |
| Alert          | alertId, type, timestamp, status                  | acknowledge(), escalate()               | Linked to Patient and Device             | Alerts must be acknowledged within 5 min. |
| Doctor         | doctorId, name, specialty, contactInfo            | reviewData(), respondToAlert()          | Monitors Patients                         | A doctor monitors multiple patients. |
| HealthRecord   | recordId, timestamp, dataType, dataValue          | addEntry(), viewHistory()               | Belongs to Patient                        | Each patient has a single health record. |
| Appointment    | appointmentId, dateTime, status                   | schedule(), cancel(), complete()        | Between Patient and Doctor               | A patient can book multiple appointments. |
| Admin          | adminId, name, role                               | manageUsers(), viewReports()            | Manages System                            | Only admin can assign doctors. |

---




