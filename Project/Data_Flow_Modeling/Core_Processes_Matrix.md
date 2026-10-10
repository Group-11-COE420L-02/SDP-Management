
# Core Processes Matrix #

## P1: Manage Teams ##

### Input Data ###
Team registration and corrections; student search criteria; team invitations and invitation responses (Student)  
Existing teams and memberships (D1)  
Student directory records (D2)  

### Output Data ###
Team registration status; student search results; team membership status (Student)  
Team and membership records (D1)  
Team invitation and membership notification events (D5)  

### Rules ###
Validate required team and project information. Add the creator as a member. Invite only students who are not in another team; add invitees only after acceptance. Determine advisor-contact eligibility using the configured minimum team size. Save valid corrections and queue invitation or membership notifications.  

## P2: Manage Profiles and Advisor Search ##

### Input Data ###
Advisor search criteria; profile requests and updates (Student)  
Professor availability; profile requests and updates (Professor)  
Profile requests and updates (SDP Coordinator)  
Profiles and available timeslots (D2)  
Current advisor assignments (D1)  

### Output Data ###
Advisor profiles and available timeslots; own profile information (Student)  
Own profile information and supervision capacity (Professor)  
Own profile information (SDP Coordinator)  
Profile and availability updates (D2)  

### Rules ###
Filter advisor results by the requested expertise. Show available timeslots and compute supervision load from current assignments; remaining capacity equals 4 minus that load. Allow users to view or update only their own editable profile details. Permit professors to maintain their own availability.  

## P3: Manage Meetings ##

### Input Data ###
Meeting requests with project and team information; meeting change requests; meeting and contact status queries (Student)  
Meeting responses; meeting change requests; meeting queries (Professor)  
Team details and membership (D1)  
Professor availability (D2)  
Existing meetings and contact history (D3)  

### Output Data ###
Meeting information and contact status (Student)  
Meeting requests with project and team information; meeting information (Professor)  
Meeting records and contact status updates (D3)  
Meeting notification events (D5)  

### Rules ###
Check team membership, advisor-contact eligibility and the selected timeslot. Reject conflicting bookings. Record meeting requests and contacted professors. Apply the addressed professor's response. Allow only participants to cancel or request rescheduling; check the new slot before confirming it. Save current meeting status and queue updates for the other participant.  

## P4: Manage Advisor Assignments ##

### Input Data ###
Advisor requests with project and team information; assignment status queries (Student)  
Student group responses; advisor confirmations; assigned team queries (Professor)  
Teams, pending advisor requests and current assignments (D1)  
Professor profile and advising availability (D2)  

### Output Data ###
Team assignment status (Student)  
Student group requests and team information; assigned team information (Professor)  
Advisor requests and assignment updates (D1)  
Advisor assignment notification events (D5)  

### Rules ###
Accept requests only from eligible teams. Allow only the addressed professor to respond. Before acceptance, check that the team has no different advisor and the professor supervises fewer than 4 teams. Save acceptance and the assignment together so concurrent requests cannot exceed the limit. Derive updated capacity from the saved assignments. Queue the mandatory acceptance notice; an optional professor confirmation must not create a duplicate assignment.  

## P5: Review and Confirm Teams ##

### Input Data ###
Team registration review decisions; team assignment decisions; correction requests; review and history queries (SDP Coordinator)  
Team registration and assignment records (D1)  
Advisor profiles and availability (D2)  
Previous review decisions (D4)  

### Output Data ###
Team registration information; team assignment information; advisor availability and capacity information; confirmation history; assignment issue reports (SDP Coordinator)  
Reviewed corrections and confirmation status (D1)  
Dated confirmation or rejection decisions and reasons (D4)  
Review decision and correction notification events (D5)  

### Rules ###
Restrict review decisions to the coordinator. Confirm only complete, valid registrations with an assigned advisor whose total load is at most 4 teams. Flag missing details, missing advisors or overload; reject invalid assignments with a reason and correction request. Validate corrections before saving them. Preserve each dated decision and queue notices for the affected students and professor.  

## P6: Manage Messages and Notifications ##

### Input Data ###
Messages and message retrieval requests (Student)  
Messages and message retrieval requests (Professor)  
User identities and recipient records (D2)  
Stored messages and pending notification events (D5)  

### Output Data ###
Messages and notifications (Student)  
Messages and notifications (Professor)  
Messages and notification delivery status (D5)  

### Rules ###
Validate the sender and intended recipient. Store messages and expose private messages only to their participants. Read queued events from P1, P3, P4 and P5, then deliver the corresponding invitation, meeting, assignment or correction notice to the affected users. Record delivery status to avoid repeatedly delivering the same event.  
