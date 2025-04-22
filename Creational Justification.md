## Creational Patterns Justification - Smart Health Care Monitoring System

This project applies six creational design patterns to enhance the flexibility and scalability of the Smart Health Care Monitoring System. Each pattern addresses specific challenges in object creation while keeping the system modular and extensible.

---

### 1. 🏢 Simple Factory

**Purpose**: Centralizes object creation without exposing instantiation logic.

**Use Case**: Create different types of `Device` objects (e.g., HeartRateMonitor, BloodPressureMonitor).

**Justification**:
- Reduces tight coupling between client code and object creation.
- Simplifies the addition of new device types.
- Provides a single entry point for device creation logic.

---

### 2. 🧱 Factory Method

**Purpose**: Allows subclasses to determine which object to instantiate.

**Use Case**: Create `Notification` objects for different channels like SMS, Email, or In-App based on alert type.

**Justification**:
- Encourages adherence to Open/Closed Principle.
- Supports pluggable extensions for communication channels.

---

### 3. 🧪 Abstract Factory

**Purpose**: Creates families of related objects without specifying concrete classes.

**Use Case**: Construct families of UI components or alert handlers that work together (e.g., alert generators + responders).

**Justification**:
- Ensures consistency across related components.
- Facilitates theme or role-specific UI/service generation.

---

### 4. 🧰 Builder

**Purpose**: Constructs complex objects step-by-step.

**Use Case**: Build a `HealthRecord` with optional fields like comments, vitals, and diagnostic reports using `HealthRecordBuilder`.

**Justification**:
- Improves readability and maintainability of object creation.
- Avoids constructor overload.
- Enables safe object construction with validation steps.

---

### 5. 🧜️ Prototype

**Purpose**: Clone existing objects instead of building from scratch.

**Use Case**: Clone standard `Alert` templates (e.g., for emergency, warning, reminder) and customize fields like `timestamp`, `recipient`, etc.

**Justification**:
- Enables reuse of predefined templates.
- Reduces time and cost of object creation.
- Useful for alerts with common configurations.

---

### 6. 🔐 Singleton

**Purpose**: Ensures one and only one instance of a class exists.

**Use Case**: Central management of `AlertDispatcher` or `SystemLogger`.

**Justification**:
- Maintains global access point for logging or alert distribution.
- Prevents inconsistency or duplication.
- Useful for managing shared system-wide services.

---

These design patterns not only streamline object creation but also align with the system's needs for reliability, extensibility, and maintainability in a healthcare context.
