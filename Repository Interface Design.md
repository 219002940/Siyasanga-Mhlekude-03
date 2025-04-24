### Generic Interface Definition
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

### Entity-Specific Interfaces 
from src.patient import Patient

class PatientRepository(Repository[Patient, str]):
    pass

    Justification: Used generics to avoid duplication across entity repositories and support polymorphism
    
