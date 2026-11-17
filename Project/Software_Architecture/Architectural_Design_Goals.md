# Architectural Design #

## Architectural Design Goals ##

| Field | Description |
|---|---|
| Goal ID | DG-01 |
| Design Goal | Maintainability |
| Description | The system can be easily fixed, changed or extended. This is achieved through a modular structure: the system is divided into separate modules (professor search, meeting scheduling, availability management, messaging, team assignment and coordinator review), so each one can be modified without changing unrelated modules. |
| Related Requirement | NFR-05 (modular structure allowing features to be modified independently). It supports FR-01, FR-02 and FR-11 to FR-19. |
| Priority | High |
| Justification | Four team members are building the system in parallel, each owning different use cases. Low coupling between modules lets each member work on their feature without breaking someone else's. The scope also leaves features for later, such as an integrated chat and Banner/Blackboard integration, so the design has to allow new modules to be added cleanly. |

| Field | Description |
|---|---|
| Goal ID | DG-02 |
| Design Goal | Security |
| Description | Only authenticated users can reach the system, and each user can only perform the actions allowed for their role. Students, professors and the Senior Design Coordinator each get different permissions, and users can't access each other's private data. |
| Related Requirement | NFR-06 (login required), NFR-10 (no access to other users' private messages), NFR-14 (only the authorized professor can accept groups), NFR-18 (only the coordinator can confirm or reject teams). It also relates to FR-06 (university email login only). |
| Priority | High |
| Justification | The system stores student personal information, project ideas and private messages. It also makes official decisions: a professor accepting a team and the coordinator confirming an assignment. If an unauthorized user could accept or confirm a team, the advisor selection process would no longer be trustworthy. |

| Field | Description |
|---|---|
| Goal ID | DG-03 |
| Design Goal | Reliability |
| Description | The system keeps its data correct and consistent at all times. A timeslot is never double-booked, a professor never goes over the team limit, capacity updates immediately, and confirmed decisions are saved permanently. |
| Related Requirement | NFR-03 (no double-booking of timeslots), NFR-13 (capacity updated immediately), NFR-15 (maximum 4 teams per professor), NFR-09 and NFR-19 (meetings and decisions persist after logout). It supports FR-13 and FR-14. |
| Priority | High |
| Justification | The main value of the system is that students can trust what they see: available timeslots and remaining capacity. If two groups booked the same slot, or a professor ended up with 5 teams, the system would cause the exact problem it was built to solve. |
