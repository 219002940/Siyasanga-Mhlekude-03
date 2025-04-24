### Abstraction Layer (Factory Pattern)

/factories/repository_factory.py


from repositories.inmemory.patient_repository import InMemoryPatientRepository

def get_patient_repository(storage_type: str = "MEMORY"):
    if storage_type == "MEMORY":
        return InMemoryPatientRepository()
    elif storage_type == "DATABASE":
        raise NotImplementedError("Database backend not implemented yet")
    else:
        raise ValueError("Invalid storage type")

        
        Justification: Chose Factory Pattern for simple backend switching and future extensibility.
