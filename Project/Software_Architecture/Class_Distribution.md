# Class Distribution

The following table assigns every class from the consolidated Lab 5 model to exactly one primary component. It uses the column format specified in Exercise 3.

| ID | Component Name | Responsibilities | Included Classes |
| --- | --- | --- | --- |
| CO1 | User Interface | Display the student, professor, and coordinator views; collect input; submit requests to the application logic layer. | None from Lab 5; presentation classes were not included in the domain model. |
| CO2 | User Management and Advisor Search | Manage accounts, authentication, role-based access, professor profiles, and advisor searches. | User, Student, Professor |
| CO3 | Meeting Scheduling | Manage schedules, availability slots, reservations, and meeting booking, confirmation, cancellation, and rescheduling. | Schedule, AvailabilitySlot, Meeting |
| CO4 | Team Assignment and Review | Manage teams, advisor requests, assignments, capacity rules, coordinator decisions, and review history. | SeniorDesignTeam, Advisor Request, AdvisorAssignment, AssignmentReview, SeniorDesignCoordinator |
| CO5 | Messaging and Notification | Manage team-professor conversations, messages, event notifications, and read status. | Chat, Message, Notification |
| CO6 | Storage | Provide persistent storage and retrieval through a single data access boundary and support transactional updates. | None from Lab 5; stores the data of the domain classes without owning those classes. |

## Distribution justification

User, Student, and Professor are grouped around shared account information and professor search. Schedule, AvailabilitySlot, and Meeting are grouped together because booking or changing a meeting must update the relevant slot and schedule consistently. SeniorDesignTeam, Advisor Request, AdvisorAssignment, AssignmentReview, and SeniorDesignCoordinator are grouped around the complete assignment and review workflow. Chat, Message, and Notification are grouped around communication and event notices.

SeniorDesignCoordinator retains its inheritance from User even though the two classes belong to different components. Student and Professor retain their existing operations and collaborate with Meeting Scheduling and Team Assignment and Review when those operations initiate a booking or assignment workflow. These relationships are represented through component interfaces in the subsequent exercises.

There are six components and fourteen assigned Lab 5 classes: three in CO2, three in CO3, five in CO4, and three in CO5. Each class has one primary owner. The name Advisor Request is retained as written in the consolidated Lab 5 model. The User Interface and Storage components require no invented Lab 5 classes.
