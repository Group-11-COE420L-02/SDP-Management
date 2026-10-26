# Integration Notes – Lab 5

## Senior Design Advisor Management System

## Overview

The individual UML Class Diagrams developed by the four team members were combined into one integrated UML Class Diagram. The integration process focused on removing duplicate classes, connecting related components, and ensuring consistency between class relationships, attributes, and methods.

The final integrated model consists of **14 classes**, including the AdvisorRequest class added during team integration.

## 1. Class Consolidation

**I01 – Duplicate User Classes**  
Retained one shared User class from Mahmoud's model for Student, Professor, and SeniorDesignCoordinator.

**I02 – Duplicate Professor Reference**  
Merged Khaled's Professor reference with Mahmoud's Professor class and connected it to Schedule.

**I03 – Classes Retained**  
Retained all 13 distinct classes from the four individual models.

**I04 – AdvisorRequest Added**  
Added AdvisorRequest to distinguish a pending advisor request from an accepted AdvisorAssignment. It connects the initiating student, team, and receiving professor.

## 2. Inheritance and Associations

**I05 – Inheritance Consolidated**  
Used User as the common superclass for Student, Professor, and SeniorDesignCoordinator.

**I06 – Team and Advisor Relationships**  
Connected students to teams and advisor assignments to teams and professors. Added `isCurrent` to distinguish active assignments from historical records.

**I07 – Review History Connected**  
Connected each AssignmentReview to its coordinator and AdvisorAssignment to maintain review decisions and reasons.

## 3. Scheduling and Communication

**I08 – Scheduling Connected**  
Connected Professor to Schedule, Schedule to AvailabilitySlot, and meetings to their team, professor, and selected timeslot.

**I09 – Messaging Connected**  
Connected teams and professors to Chat, Chat to Message, and User to sent messages.

**I10 – Notifications Connected**  
Linked notifications to recipient User accounts and to message, meeting, or assignment-review events. Each notification has one recipient and one triggering event.

## 4. System Constraints

**I11 – Constraints Documented**  

- Each student belongs to at most one team.
- Each team has at most one current advisor assignment.
- Each professor can supervise a maximum of four active teams.
- Only the owning professor can manage their schedule.
- Availability slots must not overlap.
- Each availability slot can have at most one active booking.

## 5. Method Improvements

**I12 – Method Details Extended**  
Added professor operations for accepting student teams, checking remaining capacity, and viewing assigned teams. Specified typed member lists and review-history return values.

## Conclusion

The integration process produced a unified UML Class Diagram representing the major components of the Senior Design Advisor Management System. Duplicate classes were consolidated, relationships were established between components, and system constraints were documented to ensure consistency across the final model.