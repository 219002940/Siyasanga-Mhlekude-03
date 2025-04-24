# Assignment 11: Repository Pattern for Smart Health Care Monitoring System

## Objective

This assignment implements a **repository layer** that abstracts persistence logic for domain model objects in the Smart Health Care Monitoring System. The design supports CRUD operations, encourages separation of concerns, and can easily switch to other backends (e.g., file, SQL, NoSQL).

---

## 1.  Repository Interface Design

### Generic Interface Definition

```python
from typing import TypeVar, Generic, Optional, List

T = TypeVar("T")
ID = TypeVar("ID")

class Repository(Generic[T, ID]):
    def save(self, entity: T) -> None:
        raise NotImplementedError

    def find_by_id(self, id: ID) -> Optional[T]:
        raise NotImplementedError

    def find_all(self) -> List[T]:
        raise NotImplementedError

    def delete(self, id: ID) -> None:
        raise NotImplementedError
```

### Entity-Specific Interfaces

```python
from src.patient import Patient

class PatientRepository(Repository[Patient, str]):
    pass
```

>  **Justification**: Used generics to avoid duplication across entity repositories and support polymorphism.

---


    
