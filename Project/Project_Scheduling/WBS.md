
# Work Breakdown Structure (WBS) #

## Task 1: Requirements Refinement ##
Task ID: 1  
Task Name: Requirements Refinement  
Description: Finalize requirements for students, professors, and the SDP coordinator based on the use cases and DFD.  
Predecessor(s): None  
Duration: 7 Days  

## Task 2: Database Design ##
Task ID: 2  
Task Name: Database Design  
Description: Design database tables for users, teams, professor availability, meetings, advisor assignments, messages, and confirmation history.  
Predecessor(s): 1  
Duration: 8 Days  

## Task 3: Authentication Implementation ##
Task ID: 3  
Task Name: Authentication Implementation  
Description: Implement university email login and role-based access for students, professors, and the coordinator.  
Predecessor(s): 2  
Duration: 8 Days  

## Task 4: User Profiles and Dashboards ##
Task ID: 4  
Task Name: User Profiles and Dashboards  
Description: Develop role-specific dashboards and profile viewing/editing features.  
Predecessor(s): 3  
Duration: 7 Days  

## Task 5: Team Registration and Management ##
Task ID: 5  
Task Name: Team Registration and Management  
Description: Implement team creation, member invitations, registration updates, and team membership validation.  
Predecessor(s): 4  
Duration: 10 Days  

## Task 6: Professor Search and Availability ##
Task ID: 6  
Task Name: Professor Search and Availability  
Description: Implement professor search by expertise, profile viewing, available timeslots, and supervision capacity display.  
Predecessor(s): 4  
Duration: 10 Days  

## Task 7: Meeting Scheduling ##
Task ID: 7  
Task Name: Meeting Scheduling  
Description: Implement meeting requests, professor responses, upcoming meetings, cancellation, and rescheduling. Prevent double-booking.  
Predecessor(s): 5, 6  
Duration: 10 Days  

## Task 8: Advisor Assignment Management ##
Task ID: 8  
Task Name: Advisor Assignment Management  
Description: Allow professors to review and accept student groups, update assignments, and enforce the maximum of 4 teams per professor.  
Predecessor(s): 5, 6  
Duration: 8 Days  

## Task 9: Coordinator Review and Confirmation ##
Task ID: 9  
Task Name: Coordinator Review and Confirmation  
Description: Implement coordinator review of team registrations, assignment confirmation/rejection, and correction requests.  
Predecessor(s): 8  
Duration: 8 Days  

## Task 10: Messaging Implementation ##
Task ID: 10  
Task Name: Messaging Implementation  
Description: Implement private messaging between students and professors.  
Predecessor(s): 3  
Duration: 8 Days  

## Task 11: Notification Management ##
Task ID: 11  
Task Name: Notification Management  
Description: Implement notifications for team invitations, meeting updates, advisor assignments, and coordinator decisions.  
Predecessor(s): 7, 9, 10  
Duration: 5 Days  

## Task 12: System Integration ##
Task ID: 12  
Task Name: System Integration  
Description: Integrate team management, professor search, meetings, advisor assignments, coordinator functions, and messaging.  
Predecessor(s): 7, 9, 10, 11  
Duration: 5 Days  

## Task 13: Functional Testing ##
Task ID: 13  
Task Name: Functional Testing  
Description: Test major use cases, including team registration, meeting scheduling, advisor capacity restrictions, and coordinator decisions.  
Predecessor(s): 12  
Duration: 7 Days  

## Task 14: Security and Performance Testing ##
Task ID: 14  
Task Name: Security and Performance Testing  
Description: Verify role-based permissions, message privacy, prevention of double-booking, and required response times.  
Predecessor(s): 12  
Duration: 5 Days  

## Task 15: Deployment Preparation ##
Task ID: 15  
Task Name: Deployment Preparation  
Description: Prepare the application for deployment, configure the database, and perform final system verification.  
Predecessor(s): 13, 14  
Duration: 5 Days  
