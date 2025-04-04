Here's the **Reflection** section in markdown format, based on the Assignment 8 instructions:

---

## Reflection for Assignment 8

### Choosing Granularity for States and Actions

One of the main challenges in developing the state and activity diagrams was finding the right level of granularity. Initially, I struggled with whether to break down actions into micro-level tasks or keep them broad and high-level. Too much detail made the diagrams cluttered and hard to follow, while too little left out essential behaviors and transitions.

For example, in the *Patient Monitoring* state diagram, I initially included transitions like "sensor initializes," "connection check," and "data integrity check"—which overwhelmed the diagram. Eventually, I grouped those under a single state like “Monitoring Initialized,” which struck a better balance between completeness and readability.

### Aligning Diagrams with Agile User Stories

Mapping diagrams to Agile user stories required thoughtful translation of narrative-based requirements into visual flows. User stories are typically abstract (“As a doctor, I want to view patient vitals…”), while diagrams require specific, actionable states or steps.

I had to revisit the acceptance criteria and decompose them into smaller transitions or activities. This back-and-forth helped improve consistency and traceability but was time-consuming. Ensuring each transition in the diagrams corresponded to a real action or event in a user story deepened my understanding of how visual modeling supports Agile development.

### Comparing State vs. Activity Diagrams

State diagrams and activity diagrams serve very different but complementary purposes:

| Aspect                 | State Diagrams                                   | Activity Diagrams                              |
|------------------------|--------------------------------------------------|------------------------------------------------|
| Focus                  | Object behavior over time                        | Workflow or process logic                      |
| Perspective            | "What can happen to this object?"                | "What is the sequence of steps in this task?"  |
| Use Case               | Tracking states like *Active*, *Disconnected*    | Mapping user flows like *Register Patient*     |
| Granularity            | Better for lifecycle modeling                    | Better for high-level decision and task flows  |
| Agile Linkage          | Good for system-level requirements               | Great for user stories and sprint planning     |

Using both types gave me a broader perspective: state diagrams clarified system constraints and object behavior, while activity diagrams revealed the human-centric interactions and system workflows. Together, they helped validate functional requirements, refine sprint tasks, and visualize user needs more concretely.

### Lesson Learned

Visual modeling is a powerful way to validate, communicate, and iterate on system design—but only when applied with clear intent. I learned that aligning models with Agile artifacts like user stories, and continuously adjusting for clarity and traceability, is key to successful documentation in software development.

--- 

Would you like this added to your canvas or README as well?
