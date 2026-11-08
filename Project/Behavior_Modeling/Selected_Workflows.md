# Selected Workflows

The following four use cases were selected to represent the major workflows of the Senior Design Advisor Management System. Each workflow demonstrates important system functionality and interactions between the primary actors and the system.  

### 1. UC-02: Schedule Advisor Meeting

This workflow begins when the student opens the schedule meeting page and selects a professor. The system retrieves the professor's schedule and the available timeslots, and the student views them and selects a timeslot. The system checks whether the selected timeslot is available. If it is unavailable, the system displays a timeslot-unavailable message, and the student selects another timeslot. If it is available, the system reserves the selected timeslot and creates a meeting record in parallel. The system then sends the meeting request, and the professor receives it. The student views the meeting confirmation, which ends the workflow.

### 2. UC-04: Review Meeting Requests

This workflow begins when the professor requests meeting requests. The system retrieves the pending requests, and the professor views them, reviews a meeting request, and chooses to accept or decline it. If the professor accepts, the system updates the status to accepted. If the professor declines, the system updates the status to declined. After the status is updated, two actions happen in parallel: the professor views the decision confirmation, and the system sends a notification to the student, who receives it indicating whether the meeting was accepted or declined. Once both actions are complete, the workflow ends.  

### 3. UC-12: Accept Student Group

This workflow begins when the professor requests their remaining team capacity. The system retrieves and displays the remaining team capacity, and the professor views it. The professor then chooses to accept a selected student group, and the system checks the professor’s remaining team capacity. If the capacity is 0, the system displays a capacity-limit message, the professor views it, and the workflow ends without accepting the group. If the capacity is greater than 0, the system marks the advisor request as accepted, creates an advisor assignment for the professor and team, and updates the remaining team capacity. The system then retrieves the team members and sends an acceptance notification to each of them. The team members receive the notification, and the professor views an acceptance confirmation, which ends the workflow.  

### 4. UC-17: Confirm Team Assignment

This workflow begins when the Senior Design Coordinator selects a team assignment. The system retrieves and displays the assignment details, and the coordinator reviews the team assignment to determine whether it is valid. If the assignment is invalid, the coordinator leaves it unconfirmed and the workflow ends without any change to its confirmation status. If the assignment is valid, the coordinator confirms it, and the system retrieves the team members, sets the confirmation status to confirmed, and records the confirmation decision. The system then sends a notification to each team member and the advisor, and the coordinator views the confirmation, which ends the workflow.  

### Workflow Coverage

Together, these workflows demonstrate the main processes involved in advisor selection, meeting coordination, student group acceptance, and administrative verification. They cover interactions involving students, professors, and the Senior Design Coordinator while illustrating the system's decision-making, validation, status management, and notification functionality.