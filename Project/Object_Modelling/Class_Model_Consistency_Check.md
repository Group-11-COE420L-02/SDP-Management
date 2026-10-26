# Consistency Check – Lab 5

## Senior Design Advisor Management System

## Overview

The integrated UML Class Diagram was reviewed for consistency across the individual models. The review focused on duplicate classes, inheritance, associations, multiplicities, attributes, methods, and alignment with the system's requirements.

## 1. Class Consistency

**Duplicate Classes**  
The duplicate User and Professor references were consolidated into single shared classes.  

**Class Naming**  
Class names were standardized across the integrated model to avoid conflicting definitions.  

**Class Responsibilities**  
Each class represents a distinct responsibility within the system. The final model contains 14 classes, including AdvisorRequest, which was introduced during integration.

## 2. Inheritance Consistency

**User Inheritance**  
Student, Professor, and SeniorDesignCoordinator inherit from the shared User class.  

**Shared Attributes and Methods**  
Common user information and authentication functionality are defined in User to avoid unnecessary duplication.

## 3. Association Consistency

**Student and Team**  
Each student belongs to at most one SeniorDesignTeam.  

**Professor and Schedule**  
Each professor maintains their own schedule, containing available meeting timeslots.  

**Team and Advisor Assignment**  
Each team can have at most one current advisor assignment. Historical assignments are distinguished using `isCurrent`.  

**Meeting Relationships**  
Meetings are associated with the relevant team, professor, and availability slot.  

**Messaging Relationships**  
Chats connect student teams and professors, while messages are associated with their respective chats and senders.  

**Notification Relationships**  
Each notification is associated with one recipient and one triggering event.

## 4. Multiplicity and Constraint Consistency

**Team Membership**  
A student can belong to at most one team.  

**Advisor Capacity**  
A professor can supervise a maximum of four active teams.  

**Advisor Assignment**  
Each team can have at most one current advisor assignment.  

**Schedule Ownership**  
Only the professor who owns a schedule can manage its availability slots.  

**Timeslot Availability**  
Availability slots must not overlap, and each slot can have at most one active booking.  

**Notifications**  
Each notification has exactly one recipient and one triggering event.

## 5. Attribute and Method Consistency

**Attributes**  
Attributes include visibility and data types to describe the information stored by each class.  

**Methods**  
Methods include visibility, parameter types, and return types where applicable.  

**Professor Functionality**  
Professor methods were extended to support accepting student teams, checking remaining capacity, and viewing assigned teams.  

**Shared Functionality**  
Common functionality is inherited from User, while class-specific operations remain in their respective classes.

## 6. Use Case Alignment

The integrated UML model supports the main functionality described in the project's use cases.

**Advisor Search and Meeting Requests:** UC-01 to UC-04  
**Advisor Assignment Monitoring:** UC-05  
**User Profiles and Communication:** UC-06 to UC-10  
**Student Group and Advisor Management:** UC-11 to UC-15  
**Coordinator Assignment Review:** UC-16 to UC-20  

## Conclusion

The consistency review documents how the individual UML models were consolidated into a unified class structure. Shared classes, inheritance relationships, associations, and system constraints were addressed during integration to maintain consistency across the Senior Design Advisor Management System.