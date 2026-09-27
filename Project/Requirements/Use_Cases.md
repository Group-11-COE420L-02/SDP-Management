# Use Cases #

## Mahmoud Contributions ##
### UC-01 ###
Use Case Name: Search for an Advisor  
Primary Actor: Student  
Short Description: The student searches for professors based on their areas of expertise and reviews available advisor options to find a suitable professor.  
Contributor: Mahmoud  

### UC-02 ###
Use Case Name: Schedule Advisor Meeting  
Primary Actor: Student  
Short Description: The student selects an available timeslot and submits a meeting request with a professor to discuss their Senior Design project.  
Contributor: Mahmoud  

### UC-03 ###
Use Case Name: Manage Availability  
Primary Actor: Professor  
Short Description: The professor adds, edits, or removes available timeslots that students can use when requesting meetings.  
Contributor: Mahmoud  

### UC-04 ###
Use Case Name: Review Meeting Requests  
Primary Actor: Professor  
Short Description: The professor reviews incoming meeting requests from students and accepts or declines requests based on their availability.  
Contributor: Mahmoud  

### UC-05 ###
Use Case Name: Monitor Advisor Assignments  
Primary Actor: Senior Design Coordinator  
Short Description: The coordinator reviews student groups and professor capacities to monitor which groups have advisors and which groups still need an advisor.  
Contributor: Mahmoud  

## Deema Contributions ##
### UC-06 ###
Use Case Name: View Profile  
Primary Actor: Student/Professor/Coordinator  
Short Description: All actors have a reason to view/manage their university profile within the system.  
Contributor: Deema  

### UC-07 ###
Use Case Name: Send message  
Primary Actor: Student/Professor  
Short Description: The student or professor sends a message through the website regarding their Senior Design project.  
Contributor: Deema  

### UC-08 ###
Use Case Name: Receive notifications  
Primary Actor: Student/Professor  
Short Description: The student or professor receives notifications about messages and meeting updates.  
Contributor: Deema  

### UC-09 ###
Use Case Name: Cancel or reschedule a meeting  
Primary Actor: Student/Professor  
Short Description: The student or professor selects an upcoming meeting and cancels or reschedules.  
Contributor: Deema  

### UC-10 ###
Use Case Name: View upcoming meetings  
Primary Actor: Student/Professor  
Short Description: The students or professors view their scheduled upcoming meetings.  
Contributor: Deema  

## Khaled Contributions ##
### UC-11 ###
Use Case Name: View Student Group Request  
Primary Actor: Professor  
Short Description: The professor views a student group’s advisor request, project idea, and team member information.  
Contributor: Khaled  

### UC-12 ###
Use Case Name: Accept Student Group  
Primary Actor: Professor  
Short Description: The professor accepts a student group as one of their Senior Design teams.  
Contributor: Khaled  

### UC-13 ###
Use Case Name: Check Team Capacity  
Primary Actor: Professor  
Short Description: The professor views their current number of supervised teams and remaining team capacity.  
Contributor: Khaled  

### UC-14 ###
Use Case Name: View Assigned Teams  
Primary Actor: Professor  
Short Description: The professor views the Senior Design teams that are currently assigned to them.  
Contributor: Khaled  

### UC-15 ###
Use Case Name: Send Advisor Confirmation  
Primary Actor: Professor  
Short Description: The professor optionally sends confirmation to the student group notifying them that they have been accepted as one of their Senior Design teams.  
Contributor: Khaled  

## Karim Contributions ##  
### UC-16 ###  
Use Case Name: Review Team Registration  
Primary Actor: Senior Design Coordinator  
Short Description: The coordinator reviews a team’s project title, members, assigned advisor, and current confirmation status.  
Contributor: Karim  

### UC-17 ###
Use Case Name: Confirm Team Assignment  
Primary Actor: Senior Design Coordinator  
Short Description: The coordinator confirms that a student team and its assigned advisor are correctly registered.  
Contributor: Karim  

### UC-18 ###
Use Case Name: Reject Team Assignment  
Primary Actor: Senior Design Coordinator  
Short Description: The coordinator rejects a team assignment when its information or advisor assignment is invalid or incomplete.  
Contributor: Karim  

### UC-19 ###
Use Case Name: Request Assignment Correction  
Primary Actor: Senior Design Coordinator  
Short Description: The coordinator provides a reason for rejection and requests that the relevant students or professors correct the assignment information.  
Contributor: Karim  

### UC-20 ###
Use Case Name: Review Confirmation History  
Primary Actor: Senior Design Coordinator  
Short Description: The coordinator views previous team confirmation and rejection decisions, including their dates, reasons, and statuses.  
Contributor: Karim  

# Relationships #

### R-01 ###
Base Use Case: UC-01 — Search for an Advisor  
Related Use Case: UC-02 — Schedule Advisor Meeting  
Relationship: extend  
Justification: After searching for an advisor, a student may optionally schedule a meeting with a professor. Scheduling a meeting is not required to complete the advisor search.  

### R-02 ###
Base Use Case: UC-11 — View Student Group Request  
Related Use Case: UC-12 — Accept Student Group  
Relationship: include  
Justification: A professor must view the student group request before they can accept it.  

### R-03 ###
Base Use Case: UC-12 — Accept Student Group  
Related Use Case: UC-13 — Check Team Capacity  
Relationship: include  
Justification: Accepting a student group requires the system to check that the professor has remaining team capacity.  

### R-04 ###
Base Use Case: UC-13 — Check Team Capacity  
Related Use Case: UC-14 — View Assigned Teams  
Relationship: extend  
Justification: While checking their team capacity, the professor may choose to view their assigned teams for more details.  

### R-05 ###
Base Use Case: UC-16 — Review Team Registration  
Related Use Case: UC-17 — Confirm Team Assignment  
Relationship: include  
Justification: The coordinator must review the registration before confirming it.  

### R-06 ###
Base Use Case: UC-16 — Review Team Registration  
Related Use Case: UC-18 — Reject Team Assignment  
Relationship: include  
Justification: The coordinator must review a registration before rejecting it.  

### R-07 ###
Base Use Case: UC-18 — Reject Team Assignment  
Related Use Case: UC-19 — Request Assignment Correction  
Relationship: include  
Justification: A rejection always requires requesting a correction, so the two actions are inseparable.  

### R-08 ###
Base Use Case: UC-07 — Send Message  
Related Use Case: UC-08 — Receive Notifications  
Relationship: include  
Justification: Sending a message triggers a notification for the recipient to view.  

### R-09 ###
Base Use Case: UC-10 — View Upcoming Meetings  
Related Use Case: UC-09 — Cancel or Reschedule Meeting  
Relationship: extend  
Justification: Cancelling or rescheduling a meeting requires viewing upcoming meetings first.  

### R-10 ###
Base Use Case: UC-12 — Accept Student Group  
Related Use Case: UC-15 — Send Advisor Confirmation  
Relationship: extend  
Justification: When a professor accepts a student group, they may optionally send confirmation to the student group.  
