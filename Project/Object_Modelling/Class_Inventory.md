# Class Identification – Lab 5

## Senior Design Advisor Management System

The following classes were identified during individual object modelling and consolidated during team integration.

## Mahmoud Bastouni

### C01 – User
**Class Name:** User  
**Responsibility:** Stores shared account information and provides login and logout functionality.  
**Related Use Cases:** UC-06

### C02 – Student
**Class Name:** Student  
**Responsibility:** Searches for advisors, views availability, and requests meetings.  
**Related Use Cases:** UC-01, UC-02

### C03 – Professor
**Class Name:** Professor  
**Responsibility:** Manages availability, reviews requests, accepts teams, and checks capacity.  
**Related Use Cases:** UC-01, UC-03, UC-04, UC-11 to UC-15

## Khaled Al-Shurafa

### C04 – Schedule
**Class Name:** Schedule  
**Responsibility:** Maintains a professor's meeting availability and supports adding, updating, and removing timeslots.  
**Related Use Cases:** UC-03

### C05 – AvailabilitySlot
**Class Name:** AvailabilitySlot  
**Responsibility:** Stores a dated time interval and manages reservations and releases.  
**Related Use Cases:** UC-02, UC-03

## Karim Hamdan

### C06 – SeniorDesignCoordinator
**Class Name:** SeniorDesignCoordinator  
**Responsibility:** Reviews, confirms, or rejects advisor assignments and requests corrections.  
**Related Use Cases:** UC-05, UC-16 to UC-20

### C07 – SeniorDesignTeam
**Class Name:** SeniorDesignTeam  
**Responsibility:** Stores team members, project details, and confirmation status.  
**Related Use Cases:** UC-11, UC-12, UC-14, UC-16 to UC-19

### C08 – AdvisorAssignment
**Class Name:** AdvisorAssignment  
**Responsibility:** Records a team's advisor and distinguishes current assignments from historical assignments.  
**Related Use Cases:** UC-05, UC-12 to UC-14, UC-16 to UC-20

### C09 – AssignmentReview
**Class Name:** AssignmentReview  
**Responsibility:** Stores coordinator decisions, reasons, and review dates.  
**Related Use Cases:** UC-17 to UC-20

## Deema Hafez

### C10 – Meeting
**Class Name:** Meeting  
**Responsibility:** Stores meeting details and supports confirmation, cancellation, rescheduling, and viewing.  
**Related Use Cases:** UC-02, UC-04, UC-09, UC-10

### C11 – Chat
**Class Name:** Chat  
**Responsibility:** Groups messages exchanged between a student team and a professor.  
**Related Use Cases:** UC-07

### C12 – Message
**Class Name:** Message  
**Responsibility:** Stores message content, sending time, and status.  
**Related Use Cases:** UC-07, UC-08

### C13 – Notification
**Class Name:** Notification  
**Responsibility:** Stores an event notification and its read status for one recipient.  
**Related Use Cases:** UC-08, UC-15

## Team Integration

### C14 – AdvisorRequest
**Class Name:** AdvisorRequest  
**Responsibility:** Stores a team's advisor request, its status, and acceptance or decline.  
**Related Use Cases:** UC-11, UC-12

## Conclusion

The final integrated UML Class Diagram consists of 14 classes, combining the individual contributions into a unified object model for the Senior Design Advisor Management System.