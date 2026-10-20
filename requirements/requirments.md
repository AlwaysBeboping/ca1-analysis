# Stakeholders & Requirements

## Classify Statements 
| Statement | Classification | Reason | 
| ----------- | ----------- | ----------- | 
| Fixture details are copied into different spreadsheets       | Problem evidence | Describes the current situation of fragmentation data management |  
| A venue must not exceed the approved capacity                | Business Rule    | An organizational policy which must always be enforced           |  
| The initial service must be accessible through a web browser | Constraint       | Restricts how the solution may be delivered                      |  
| Existing club records may contain duplicate contact details  | Risk             | Uncertainty may negatively affect implementation                 |   
| Every club has access to an email                            | Assumption       | Believed to be true but requires verification                    |   
<br>



## Business Problem Statement
<div style="text-align: justify">
<p>
Kerry Youth Sports League uses paper forms, spreadsheets and messages to manage clubs, teams, fixtures, venues, officials and results across several age group competitions. Information is fragmented across several records and communication channels such as paper forms, spreadsheets and phone messages and is entered manually into different spreadsheets by different staff members. Staff cannot reliably prevent conflicting venues/officials/fixtures, teams must contact staff to check availability and fixtures require manual maintenance.
</p> 
<p>
Staff struggle to distinguish initial interest, missing evidence and readiness for a decision. These issues increase administrative effort, reduce confidence in the leagues records and may result in an inconsistent service for clubs. The proposed Sports League Management System will manage clubs and their respective teams  with searchable fixtures, fixture results, available venues, available officials and basic management reporting. Team managers also recieve fixture information in different formats making fixture mangement inefficient and increasing the likelihood for errors.
</p>
</div><br>

# Propose Statement 
<div style="text-align: justify">
The proposed Youth Sports League Management System will support team entries, venue availability, venue bookings, official availability, official appointments, team records, coordinate fixtures and basic operational reporting.
</div><br>

## Scope

| In Scope | Out of Scope |
| ----------- | ----------- |
| Team Records                       |  Staff payroll               |
| Venue Availability & Bookings      | Equipment Purchasing         |
| Match Official Appoinments         | Supplier Management          |
| Team Registration                  | Venue-access control         |
| Team Fixtures                      | Team-stats integration       |
| Eligibility info                   | Native mobile application    |
| Basic League Reports               | Full public website redesign |
<br>

## Stakeholder Analysis

| Stakeholder | Goals | Concerns |  Influence | Expected Interaction |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| Club Representative       |    Register Team                        |  Availability & accurate league info           | Medium | View availability, Register/Deregister |
| Player                    |    View Fixtures & Results              |  Accurate league info                          | Medium | View upcoming Fixtures/results         |
| League Staff              |    Process requests efficiently         |  Conflicts & incomplete/inaccurate info        |  High  | Maintain Players & bookings            |
| System Admin              |    Maintain secure & reliable access    |  Security & availability of accounts           | Medium | Manage access & system                 |
| Coordinator               |    Coordinate feasible fixtures.        |  Venues/officials availability and  match info |  High  | Allocate fixtures                      |
| League Manager            |    Monitor activity & usage             |  Reliable reports & operation costs            | Medium | View & export reports                  |
| Data Protection Officer   |    Ensure appropriate data processing   |  Privacy retention & role access               |  High  | Review requirements & evidence         |
| Match Official            |    Recieve appointments when available  |  Appointment clashes & schedule changes        |  High  | Provide availiablity & recieve updates |
| Funders                   |    Assess how funding supports the service |  Incomplete or inconsistent reporting       |  High  | Receive summary reports on service     |


<br>

## Functional Requirements

| ID | Functional Requirement | Priority |  Source |
| ----------- | ----------- | ----------- | ----------- |
| FR01 |    The system shall authorize reception staff to register a new club                                          |  Must    |   League staff   |
| FR02 |    The system shall allow an active Club view available matches for a selected date &  time                   |  Must    |      Club        |
| FR03 |    The system shall prevent two confirmed matches from occupying the same facility during overlapping periods |  Must    |   Coordinator    | 
| FR04 |    The system shall allow the coordinator to provisionally allocate a venue                                   |  Must    |   Coordinator    |
| FR05 |    The system shall record fixture postponements or cancellations, their reasons and the decision status      |  Must    |   League staff   |
| FR06 |    The system shall ecording unallocated requests and why they remain unallocated                             |  Should  |   League Staff   |
| FR07 |    The system shall record the team, venue, start time, end time and status for each fixture                  |  Must    |   League Staff   | 
| FR08 |    The system shall allow the manager to generate a venue-usage report for a selected date range              |  Could   |  League Manager  | 
<br>

## Non-Functional Requirements

| ID | Quality Category | Measurable Requirment | 
| ----------- | ----------- | ----------- |
| NFR01 | Performance   | Venue-availability results shall be displayed within three seconds for at least 95% of requests under normal operating conditions  |
| NFR02 | Security      | Players contact and emergency information will only be available to authenticated users with authorised permissions                |
| NFR03 | Availability  | The system shall be available during league operating hours excluding scheduled maintenance announced at least 24 hours in advance | 
| NFR04 | Accessability | All participant registration functions shall be operable using a keyboard-only navigation                                          |
<br>


## Rules, Assumptions, Constraints and Risks

| Type | Statement |
| ----------- | ----------- |
| Business Rule  | A venue may not exceed its approved capacity                                 |
| Business Rule	 | Players must satisfy any age requirements before registration                |
| Business Rule  | The leagues require some proof of prior experience before a club is accepted |
| Business Rule  | A suspended team cannot book a new fixture                                   |
| Assumption     | Every unique player has a unique membership number                           |
| Assumption     | League staff have supported web browsers.                                    |
| Constraint     | Existing membership records must be imported                                 |
| Risk           | Existing spreadsheets may contain duplicates                                 |
<br>

## Stakeholder Clarification Questions

| Question Number  | Question |
| ----------- | ----------- |
| 1. | What info and eligibility evidence must be recorded for each team entry before a fixture can be confirmed?                |
| 2. | Who may approve fixture postponements or cancellations, and how should affected clubs, venues and officials be notified?  |
| 3. | What information should league managers and funders receive in summary reports?                                           |
| 4. | What evidence of authority is required before detailed information or decisions can be shared with a representative?      |
| 5. | When should provisional allocations be reviewed or released, and who is responsible for that decision?                    |
<br>