
## Reflection Assignment 9

Designing the domain model and class diagram for the Smart Health Care Monitoring System was both a rewarding and challenging experience. One of the primary challenges I encountered was deciding the level of abstraction to apply. It was tempting to model everything in detail, but I had to strike a balance between precision and readability. For example, splitting out roles like `Nurse` or `Technician` was an option, but I opted to keep only `Doctor` and `Admin` to reduce complexity.

Relationships between classes were another tricky area. Initially, I debated whether `HealthRecord` should be a composition within `Patient` or a separate class. By keeping it separate, I maintained flexibility for future updates, such as integration with hospital databases or other systems.

Defining methods was also complex. Deciding what actions belong to each class required me to revisit my use cases (Assignment 5) and user stories (Assignment 6). For instance, `schedule()` and `cancel()` clearly fit within the `Appointment` class, but where should actions like `sendData()` belong? I assigned them to `Device` after aligning them with earlier behavioral models (Assignment 8).

Comparing this approach to other tools like Trello or Jira, GitHub offers a more code-focused environment. Trello is excellent for quick visualization, but lacks the deeper integration with development artifacts. Jira excels in task tracking and reporting but can be overwhelming for smaller projects. GitHub, while simpler, aligns naturally with markdown and Mermaid.js, making it ideal for modeling alongside the repository.

Another key insight came from comparing the state diagrams (Assignment 8) to the class diagram. State diagrams help visualize the life cycle of a single object, like how an `Alert` moves from `New` to `Acknowledged` or `Escalated`. In contrast, class diagrams reveal structural relationships between all entities. Both are essential: state diagrams show behavior over time, while class diagrams highlight static relationships and data structures.

I also learned that Agile alignment doesn't mean skipping documentation; rather, it means generating **just enough** design to support development. My domain model directly ties into user stories, and the class diagram supports sprint planning and task decomposition.

In conclusion, this assignment reinforced core object-oriented principles like encapsulation, abstraction, and clear responsibility allocation. It also improved my ability to model systems both visually and logically. I now appreciate the balance needed between simplicity and completeness, especially when diagrams serve as both design and communication tools.


