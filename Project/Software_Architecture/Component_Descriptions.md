# Identify Components and Distribute Project Classes

## Component descriptions

The system uses six software components organized within the three-layer architecture selected in Exercise 2. The presentation layer contains the User Interface component. The application logic layer contains User Management and Advisor Search, Meeting Scheduling, Team Assignment and Review, and Messaging and Notification. The data layer contains the Storage component.

### CO1 User Interface

**Layer:** Presentation layer.

**Responsibilities:** Present information to students, professors, and the senior design coordinator, collect user input, and send requests to the application logic layer. The Student Interface, Professor Dashboard, and Coordinator Dashboard are views within this component.

**Supported functionality:** Login forms, professor search screens, availability and meeting screens, team request and assignment screens, coordinator review screens, and message and notification displays. Business rules and authorization are enforced by the application logic layer.

**Included classes:** None from Lab 5. The consolidated class diagram models domain classes rather than user interface classes.

### CO2 User Management and Advisor Search

**Layer:** Application logic layer.

**Responsibilities:** Manage shared account information, authenticate users, enforce role-based access, and provide professor search and profile information. This component combines the Authentication & Access Control and Advisor Search functions described in Exercise 2.

**Supported functionality:** University account login and logout, user identity and role validation, searching professors by expertise, and retrieving professor information. Student and professor operations involving meetings or team acceptance coordinate with the components responsible for those workflows through defined interfaces.

**Included classes:** User, Student, Professor.

### CO3 Meeting Scheduling

**Layer:** Application logic layer.

**Responsibilities:** Manage professors' schedules, availability slots, and meetings. Keep slot reservations consistent with meeting status, prevent overlapping availability slots, and prevent more than one active booking for a slot.

**Supported functionality:** Add, update, remove, and view availability slots; check and reserve available slots; request and confirm meetings; cancel and reschedule meetings; release cancelled bookings; and view meeting details. Only the owning professor may modify a schedule.

**Included classes:** Schedule, AvailabilitySlot, Meeting.

### CO4 Team Assignment and Review

**Layer:** Application logic layer.

**Responsibilities:** Manage teams, advisor requests, accepted advisor assignments, and coordinator review decisions. This component combines the Team Assignment and Assignment Review functions described in Exercise 2. It keeps pending advisor requests separate from accepted assignments and preserves assignment and review history.

**Supported functionality:** Store team members and project details; submit, accept, or decline advisor requests; check the maximum of four active teams per professor; create advisor assignments; maintain one current assignment per team; and let the authorized coordinator review, confirm, reject, or request corrections to assignments. Record decision reasons and dates and retrieve previous decisions.

**Included classes:** SeniorDesignTeam, Advisor Request, AdvisorAssignment, AssignmentReview, SeniorDesignCoordinator.

### CO5 Messaging and Notification

**Layer:** Application logic layer.

**Responsibilities:** Manage conversations between teams and professors, store messages and their status, and manage notifications for individual recipients. Restrict access to private conversations to authorized participants.

**Supported functionality:** Add, send, and view chat messages; update message status; create notices for message, meeting, and assignment-review events; display notifications; and mark notifications as read. Each notification has one recipient and one triggering event. This component also coordinates email notification delivery.

**Included classes:** Chat, Message, Notification.

### CO6 Storage

**Layer:** Data layer.

**Responsibilities:** Provide a single controlled route for reading and writing persistent data. Store users, schedules, slots, meetings, teams, requests, assignments, reviews, chats, messages, and notifications in the relational database.

**Supported functionality:** Save and retrieve records, preserve meetings and decisions after logout, and execute related updates in transactions. Transactional booking and assignment updates support the rules against double-booking and exceeding professor capacity.

**Included classes:** None from Lab 5. The domain classes remain owned by their application logic components; storing their data does not give Storage a second ownership of those classes. Persistence implementation classes can be introduced during detailed design.

## Component organization

The User Interface calls the application logic layer, and application logic components access persistent data through Storage. The User Interface does not access the database directly. Components within the application logic layer collaborate through defined interfaces; a reference to a class owned by another component does not duplicate that class's ownership.

The three user dashboards form one presentation component, authentication and advisor search form one application component, and team assignment and coordinator review form one application component. This grouping retains the functionality of Exercise 2 while meeting the requirement of four to six architectural components.
