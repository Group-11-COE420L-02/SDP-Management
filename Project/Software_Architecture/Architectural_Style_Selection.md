# Architectural Style #

### 1. Selected Architectural Style ###

**3-Layer (three-tier) architecture.** It is deployed as a web client/server system: the browser is the client, and the server hosts the application logic and data layers.

| Layer | Subsystems (Components) |
|---|---|
| Presentation Layer | Student Interface, Professor Dashboard, Coordinator Dashboard |
| Application Logic Layer | Authentication & Access Control, Advisor Search, Meeting Scheduling (Schedule, AvailabilitySlot, Meeting), Team Assignment (accept group, capacity check), Assignment Review (coordinator confirm/reject), Messaging & Notification |
| Data Layer | Storage subsystem → Database (users, professors, teams, meetings, messages, assignments) |

### 2. Main Characteristics ###

- The system is divided into three layers, each with one responsibility: showing information, applying business rules, and storing data.
- Layering is closed: each layer only calls the layer directly below it through defined interfaces. The user interface never accesses the database directly.
- Inside the application logic layer, components are grouped around related classes (high coherence). For example, Schedule, AvailabilitySlot and Meeting form the Meeting Scheduling component.
- All data access goes through a single Storage subsystem (indirect access to the database through Storage).

### 3. Why It Is Appropriate for the Project ###

- The project is a standard web application with three user roles (students, professors and the Senior Design Coordinator) who all share the same data. A browser-based interface, a server with business rules and a central database map directly onto three layers.
- The team's planned technology stack (Angular front end, ASP.NET back end, relational database, as stated in the Feasibility Study) already follows this separation.
- The major deliverables in the Scope (three dashboards, a database and an email notification system) fit naturally into the presentation, data and application logic layers.
- The work can be divided by layer and by component, matching how the team already split the use cases (Mahmoud: search and scheduling, Deema: messaging and meetings, Khaled: team acceptance, Karim: coordinator review).

### 4. How It Supports the Design Goals ###

- **DG-01 Maintainability:** Each feature is its own component in the application logic layer, with a narrow interface (for example, IMeetingScheduling or ITeamAssignment). Changing the search filters does not affect meeting scheduling, and the user interface can be redesigned without touching business rules, which satisfies NFR-05.
- **DG-02 Security:** Every request passes through the Authentication & Access Control component in the application logic layer before reaching any data. Role checks happen in one place: only professors can accept groups, and only the coordinator can confirm or reject assignments. Because the presentation layer cannot reach the database directly, it cannot bypass these checks.
- **DG-03 Reliability:** The rules (no double-booking, maximum 4 teams, immediate capacity update) are enforced on the server in the application logic layer, so a modified or outdated client cannot skip them. The Storage layer saves bookings and decisions using transactions, so they persist after logout (NFR-09, NFR-19).

### 5. Advantages and Limitations ###

**Advantages**

- Clear separation of concerns, which makes the system easier to understand, test and maintain.
- Low coupling between layers, so one layer can be replaced (for example, a new user interface or a different database) with little impact on the others.
- Security and business rules are centralized on the server.
- Team members can develop and test components in parallel.
- It is a well-known style that the team's chosen frameworks support directly.

**Limitations**

- Each request passes through every layer, which adds some overhead. This is acceptable at the system's scale.
- Adding a new data field (for example, a new professor attribute) usually requires changes in all three layers.
- A single server and database is a single point of failure, which conflicts with 24/7 availability (NFR-04) unless backups or a hosted server are added later.
- Business logic can leak into the presentation layer if the team does not follow the layering rules strictly.
- More upfront design is needed, as well as learning time for team members who are new to Angular and ASP.NET (as noted in the Feasibility Study).