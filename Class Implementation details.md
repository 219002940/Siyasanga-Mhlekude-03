# Programming Language and Key Design Decisions

## Programming Language: Python

The programming language chosen for this assignment is **Python**. This decision was based on several key factors:

- **Object-Oriented Programming (OOP) Capabilities:** Python fully supports OOP principles, allowing for the creation of classes, objects, inheritance, polymorphism, and encapsulation. This paradigm is well-suited for modeling real-world entities like patients, devices, alerts, and appointments—making the codebase more organized and maintainable.

- **Readability and Simplicity:** Python's syntax is known for its clarity and conciseness. This makes the code easier to write, understand, and debug, which is particularly beneficial for a project involving multiple classes and their interactions.

- **Extensive Standard Library:** Python's rich standard library provides a wide range of built-in modules that can simplify various tasks, although for this core class implementation, we primarily focused on fundamental OOP features.

- **Large and Active Community:** The vast Python community provides ample resources, documentation, and support, making it easier to find solutions to potential issues and learn best practices.

- **Rapid Development:** Python's high-level nature allows for quicker development cycles, enabling a faster translation of the design into functional code.

---

## Key Design Decisions in Class Implementation

The design of the classes within the `src` directory was guided by the following key decisions:

### 1. Encapsulation and Information Hiding

- **Attributes:** Where appropriate, attributes were treated as private or protected (using Python’s convention of a single or double underscore prefix, e.g., `_name`, `__patient_id`). This encapsulates the internal state of objects and protects them from unauthorized modification.

- **Getters and Setters:** Getter and setter methods (e.g., `get_name()`, `set_name(new_name)`) were used when validation or encapsulated access was required. These were applied selectively, not universally, to reduce code bloat.

### 2. Modeling Real-World Entities

- Each class (`Patient`, `Doctor`, `Device`, `Alert`, `HealthRecord`, `Appointment`, `Admin`) was designed to mirror its real-world counterpart in a healthcare environment.

- Attributes represent essential properties of these entities, while methods define their behaviors and responsibilities (e.g., `send_data()` for `Device`, `acknowledge()` for `Alert`).

### 3. Relationships Between Classes

- **Associations:** Associations were used where objects reference others (e.g., a `Doctor` monitors multiple `Patients`).

- **Composition:** `Patient` objects include `HealthRecord`, `Device`, and `Alert` as part of their definition, reflecting ownership and lifecycle dependency.

- **Aggregation:** `Appointment` aggregates both `Patient` and `Doctor`, showing a shared relationship for a specific timeframe.

### 4. Method Design and Behavior

- Methods were designed around core responsibilities. For example, the `Appointment` class includes methods such as `schedule()`, `cancel()`, and `complete()`.

- Each method was made as modular and specific as possible, often using parameters to maintain clarity and flexibility.

### 5. Modularity and Organization

- All class implementations were placed in the `/src` directory for clarity and maintainability.

- Classes are kept in separate files (e.g., `patient.py`, `doctor.py`) to follow Python's single-responsibility principle.

- This layout allows for clean import paths and supports future scalability (e.g., integration with UI modules, REST APIs).

---

These design decisions ensured the class structure was **logical, modular, testable, and aligned with the object-oriented principles** critical to building an effective and scalable health monitoring system in Python.
