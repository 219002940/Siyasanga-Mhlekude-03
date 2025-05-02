
## 2. REST API Development

### Structure

```
/api
  ├── patient_api.py
  ├── doctor_api.py
  └── appointment_api.py
```

### Example: `patient_api.py`

```python
from fastapi import APIRouter, HTTPException
from services.patient_service import PatientService

router = APIRouter()
service = PatientService()

@router.post("/api/patients")
def create_patient(patient_id: str, name: str, age: int, gender: str, contact_info: str):
    try:
        return service.create_patient(patient_id, name, age, gender, contact_info)
    except ValueError as e:
        raise HTTPException(status_code=400, detail=str(e))

@router.get("/api/patients/{patient_id}")
def get_patient(patient_id: str):
    patient = service.get_patient(patient_id)
    if not patient:
        raise HTTPException(status_code=404, detail="Patient not found")
    return patient
```

> FastAPI auto-generates `/docs` with Swagger UI.

### Integration Tests: `/tests/api/test_patient_api.py`

```python
from fastapi.testclient import TestClient
from main import app

client = TestClient(app)

def test_create_and_fetch_patient():
    response = client.post("/api/patients", params={
        "patient_id": "P002", "name": "Sam", "age": 31, "gender": "M", "contact_info": "sam@mail.com"
    })
    assert response.status_code == 200
    patient = client.get("/api/patients/P002")
    assert patient.status_code == 200
```

---



