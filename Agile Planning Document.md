# Agile Planning Document for Smart Healthcare Monitoring System(Assignment 6)

## 1. Introduction
This document consolidates all **Agile planning artifacts** for the **Smart Healthcare Monitoring System**, ensuring traceability between **requirements, user stories, backlog prioritization, and sprint planning**.

---

## 2. Traceability Matrix (User Stories to Requirements)

| User Story ID | User Story | Requirement ID | Requirement Description |
|--------------|-----------|---------------|--------------------------|
| US-001 | As a doctor, I want to view real-time patient vitals so that I can make quick medical decisions. | FR-001 | The system shall collect patient vitals from IoT devices. |
| US-002 | As a nurse, I want to acknowledge and dismiss alerts so that I can manage patient care efficiently. | FR-003 | The system shall trigger alerts when abnormal vitals are detected. |
| US-003 | As a patient, I want my vitals securely stored so that my medical data remains private. | FR-006 | The system shall store patient vitals securely in a database. |
| US-004 | As an IT staff member, I want to integrate the system with hospital databases so that we can maintain data consistency. | FR-007 | The system shall integrate with existing hospital management systems. |
| US-005 | As a hospital administrator, I want to manage user roles so that only authorized personnel can access patient data. | FR-008 | The system shall support access control based on user roles. |
| US-006 | As a family member, I want to request patient updates so that I can stay informed about my relative’s condition. | FR-009 | The system shall provide historical data for analysis. |
| US-007 | As a regulatory officer, I want to generate compliance reports so that we can meet healthcare regulations. | FR-010 | The system shall generate automated reports on patient health trends. |
| US-008 | As a system admin, I want user activity logs so that security incidents can be audited. | NFR-002 | The system shall log all access attempts for auditing. |

---

## 3. Product Backlog

| Story ID | User Story | Priority (MoSCoW) | Effort Estimate | Dependencies |
|----------|-----------|------------------|----------------|--------------|
| US-001 | View real-time patient vitals | Must-have | 5 | IoT data streaming |
| US-002 | Acknowledge and dismiss alerts | Must-have | 3 | US-001 |
| US-003 | Store vitals securely | Must-have | 4 | Database encryption module |
| US-004 | Integrate system with hospital database | Should-have | 5 | US-003 |
| US-005 | Manage user roles | Must-have | 3 | Authentication system |
| US-006 | Request patient updates | Could-have | 2 | US-005 |
| US-007 | Generate compliance reports | Should-have | 4 | Data storage system |
| US-008 | Maintain user activity logs | Must-have | 4 | Authentication & database |

---

## 4. Sprint Planning

### **Sprint Goal:**
*“Implement real-time vitals monitoring, alert handling, and secure data storage.”*

### **Sprint Backlog**

| Task ID | Task Description | Assigned To | Estimated Hours | Status |
|---------|-----------------|-------------|----------------|--------|
| T-001 | Develop real-time vitals streaming | Backend Team | 8 | To Do |
| T-002 | Implement alert handling system | Backend Team | 6 | To Do |
| T-003 | Encrypt patient vitals storage | Security Team | 5 | To Do |
| T-004 | Develop role-based access control | DevOps | 6 | To Do |
| T-005 | Design dashboard UI for vitals monitoring | Frontend Team | 7 | To Do |
| T-006 | Develop API endpoint for fetching vitals | Backend Team | 6 | To Do |

---

## 5. Conclusion
This document ensures **traceability, clarity, and alignment** with Agile best practices. It links **user stories to system requirements**, prioritizes backlog items, and structures **sprint execution** effectively.
