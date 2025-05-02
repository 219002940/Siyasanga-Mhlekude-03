# Assignment 12: Service Layer and REST API for Smart Health Care Monitoring System

## 🔍 Objective

Build a service layer to encapsulate business logic and expose it via a REST API using FastAPI. The solution will cover three core entities:

* `Patient`
* `Doctor`
* `Appointment`

This solution builds on:

* Repository Layer (Assignment 11)
* Domain and Class Models (Assignments 9–10)

---

## 1.Service Layer Implementation

### Structure

```
/services
  ├── patient_service.py
  ├── doctor_service.py
  └── appointment_service.py
```

### Example: `patient_service.py`

```python
from repositories.inmemory.patient_repository import InMemoryPatientRepository
from src.patient import Patient

class PatientService:
    def __init__(self):
        self.repo = InMemoryPatientRepository()

    def create_patient(self, patient_id, name, age, gender, contact_info):
        if self.repo.find_by_id(patient_id):
            raise ValueError("Patient already exists")
        patient = Patient(patient_id, name, age, gender, contact_info)
        self.repo.save(patient)
        return patient

    def get_patient(self, patient_id):
        return self.repo.find_by_id(patient_id)

    def delete_patient(self, patient_id):
        self.repo.delete(patient_id)
```

> Similar services exist for `DoctorService` and `AppointmentService`.

### ✅ Unit Tests: `/tests/services/test_patient_service.py`

```python
from services.patient_service import PatientService

service = PatientService()
patient = service.create_patient("P001", "Jane", 29, "F", "jane@mail.com")
assert service.get_patient("P001") == patient
service.delete_patient("P001")
assert service.get_patient("P001") is None
```

---

