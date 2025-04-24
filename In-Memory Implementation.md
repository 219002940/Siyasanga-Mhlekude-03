
---

## 2.  In-Memory Implementation

### `/repositories/inmemory/patient_repository.py`

```python
from typing import Dict, Optional, List
from src.patient import Patient
from repositories.patient_repository import PatientRepository

class InMemoryPatientRepository(PatientRepository):
    def __init__(self):
        self._storage: Dict[str, Patient] = {}

    def save(self, entity: Patient) -> None:
        self._storage[entity.patient_id] = entity

    def find_by_id(self, id: str) -> Optional[Patient]:
        return self._storage.get(id)

    def find_all(self) -> List[Patient]:
        return list(self._storage.values())

    def delete(self, id: str) -> None:
        self._storage.pop(id, None)
```

> Includes similar implementations for Doctor, Device, Alert, etc.

