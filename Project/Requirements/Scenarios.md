# Scenarios #
## S-01: Finding and Contacting a Senior Design Advisor ##
### Actor/Stakeholder: Student ###
### Scenario Description: ###

1. Mahmoud logs into the SDP Management System with his Student Account.
2. Mahmoud searches for professors whose areas of expertise are related to his group's project.
3. The system displays a list of matching professors along with their areas of expertise, availability, and current number of supervised teams.
4. Mahmoud selects a professor that is available and in the suitable area of expertise.
5. Mahmoud views the selected professors schedule and selects an available timeslot.
6. Mahmoud enters his team’s project idea and adds the names of his team members.
7. The system sends the meeting request and project information to the professor and adds the professor to Mahmouds list of contacted professors.

## S-02: Cancelling and Rescheduling a Meeting ##
### Actor/Stakeholder: Student/Professor
### Scenario Description: ###

1. Deema logs into the SDP Management System.
2. Deema opens the list of upcoming meetings.
3. Deema selects the meeting she wants to change.
4. Deema chooses to cancel the meeting or request a different available time.
5. The system updates the meeting information.
6. The system notifies the other user about the cancellation or rescheduling request.
7. If the meeting is rescheduled, the updated meeting time will be shown in both users’ upcoming meetings.

## S-03: Accepting a Student Group for Senior Design ##
### Actor/Stakeholder: Professor / Student ###
### Scenario Description: ###

1. Professor logs into the SDP Management System.
2. Professor views a student group's advisor request and project information.
3. Professor reviews the project idea and team members.
4. Professor accepts the student group as one of their Senior Design teams.
5. Then the system checks that the professor has not reached the maximum of 4 supervised teams.
6. System assigns the professor as the group's advisor.
7. System updates the professor's remaining capacity and notifies the student group that their advisor has been confirmed.

## S-04: Confirming Teams and Their Advisors ##
### Actor/Stakeholder: Senior Design Coordinator ###
### Scenario Description: ###

1. The coordinator logs into the SDP Management System using their coordinator account.
2. The coordinator opens the list of registered senior design teams.
3. The system displays each team’s name, team members, project title, assigned advisor, and assignment status.
4. The coordinator reviews each team to check that all team members are correctly registered and that an advisor has been assigned.
5. The system highlights teams with missing information, no assigned advisor, or an advisor who has reached the maximum number of supervised teams.
6. The coordinator corrects any inaccurate information or contacts the relevant students and professors to resolve the issue.
7. The coordinator confirms the teams whose information and advisor assignments are valid.
8. The system updates their status to be confirmed and notifies the relevant students and advisors.

## S-05: Creating a Senior Design Team ##
### Actor/Stakeholder: Student ###
### Scenario Description: ###

1. Karim logs into the SDP Management System with his Student Account.
2. Karim selects the option to create a new Senior Design team.
3. The system displays a team creation form where Karim enters the team’s name and project idea.
4. Karim enters the required information and creates the team.
5. The system creates the team and assigns Karim as a member of the team.
6. Karim selects the option to invite students to his team.
7. Karim searches for students by their names.
8. The system displays the matching students and indicates which students are already members of another team.
9. Karim selects students who are not currently members of another team and sends them invitations to join his team.
10. The system notifies the invited students about the team invitation.
11. The invited students view the invitation and choose to accept or decline it.
12. The system updates the team member list based on their responses.
13. Once the minimum required number of members is reached, the team becomes eligible to search for and contact a Senior Design advisor.