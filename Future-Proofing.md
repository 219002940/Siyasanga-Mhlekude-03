
---

## 4. 🏢 Future-Proofing

### Stub: `/repositories/filesystem/patient_file_repository.py`

```python
import json
from src.patient import Patient

class FileSystemPatientRepository:
    def __init__(self, file_path: str):
        self.file_path = file_path

    def save(self, entity: Patient) -> None:
        raise NotImplementedError

    def find_by_id(self, id: str):
        raise NotImplementedError
```

> ✅ Stub created to enable future JSON/XML-based storage.

### 📈 Updated Class Diagram (Conceptual)

```
Repository<T, ID>
 |
 --> PatientRepository
       |
       --> InMemoryPatientRepository
       --> FileSystemPatientRepository (stub)
```

---

## 5. 🔧 Unit Tests

### `/tests/test_patient_repository.py`

```python
from repositories.inmemory.patient_repository import InMemoryPatientRepository
from src.patient import Patient

repo = InMemoryPatientRepository()

p1 = Patient("P001", "John Doe", 32, "Male", "john@example.com")
repo.save(p1)
assert repo.find_by_id("P001") == p1

repo.delete("P001")
assert repo.find_by_id("P001") is None
```

---

## 🔍 README Update Snippet

```markdown
### 🗃️ Repository Layer
- Abstracted CRUD logic via generic repository interface.
- Used Factory Pattern to switch storage types.
- Added `/repositories` for interfaces and `/inmemory` for in-memory stores.
- Future-proof: `/filesystem` folder contains JSON stub implementations.
```

---

## 🎓 Summary

- ✅ Used generic base interfaces for reuse
- ✅ Implemented working in-memory repositories
- ✅ Abstracted storage via Factory Pattern
- ✅ Prepared JSON-based storage for future
- ✅ Passed unit tests for CRUD operations

> This makes the system scalable, testable, and decoupled from backend-specific code.

