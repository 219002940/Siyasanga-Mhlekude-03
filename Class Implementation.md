## Assingment 10
## 🔧 Language Choice & Design Decisions

### 💬 Why Python?
Python was chosen for implementing the Smart Health Care Monitoring System because:
- It is concise and easy to read.
- It supports rapid prototyping.
- It has strong community support for testing and object-oriented design.

### ⚙️ Design Choices
- **Encapsulation**: Sensitive fields are marked private with double underscores.
- **Composition**: `Patient` aggregates `Device`, `Alert`, and `HealthRecord`.
- **Association**: Doctors monitor multiple patients via indirect references.
- **Responsibility Allocation**: Each class owns only relevant logic (e.g., `Alert.escalate()`, `Device.send_data()`).
