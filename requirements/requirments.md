# Requirements

## Classify Statements
 Statement | Classification | Reason | 
| ----------- | ----------- | ----------- | 
| Fixture details are copied into different spreadsheets       | Problem evidence | Describes the current situation of fragmentation data management |  
| A venue must not exceed the approved capacity                | Business Rule    | An organizational policy which must always be enforced           |  
| The initial service must be accessible through a web browser | Constraint       | Restricts how the solution may be delivered                      |  
| Existing club records may contain duplicate contact details  | Risk             | Uncertainty may negatively affect implementation                 |   
| Every club has access to an email                            | Assumption       | Believed to be true but requires verification                    |   
<br/>



## Business Problem Statement
<div style="text-align: justify">
Kerry Youth Sports League uses paper forms, spreadsheets and messages to manage clubs, teams, fixtures, venues, officials and results across several age group competitions. Information is fragmented across several records and communication channels such as paper forms, spreadsheets and phone messages and is entered manually into different spreadsheets by different staff members. Staff cannot reliably prevent conflicting venues/officials/fixtures, teams must contact reception to check availability and fixtures require manual maintenance. Management also has difficulty producing accurate information about venue use, fixtures and league activity. These issues increase administrative effort, reduce confidence in the leagues records and may result in an inconsistent service for clubs. The proposed Sports League Management System will manage clubs and their respective teams  with searchable fixtures, fixture results, available venues, available officials and basic management reporting.
</div></br>

# Propose Statement 
<div style="text-align: justify">
The proposed Youth Sports League Management System will support team entries, venue availability, venue bookings, official availability, official appointments, team records, coordinate fixtures and basic operational reporting.
</div></br>

## Scope

| In Scope | Out of Scope |
| ----------- | ----------- |
| Team Records                       |  Staff payroll               |
| Venue Availability                 | Equipment Purchasing         |
| Venue Bookings & Availability      | Supplier Management          |
| Team Registration                  | Venue-access control         |
| Team Fixtures                      | Team-stats integration       |
| Eligibility info                   | Native mobile application    |
| Basic League Reports               | Full public website redesign |
<br/>

## Stakeholder Analysis

| Stakeholder | Goals | Concerns |  Influence | Expected Interaction |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| Club                      |    Register Team                        |  Availability & accurate league info           | Medium | View availability, Register/Deregister |
| Player                    |    View Fixtures & Results              |  Accurate league info                          | Medium | View upcoming Fixtures/results|
| Reception Staff           |    Process requests efficiently         |  Conflicts & incomplete/inaccurate info        |  High  | Maintain Players & bookings   |
| System Admin              |    Maintain secure & reliable access    |  Security & availability of accounts           | Medium | Manage access & system        |
| Coordinator               |    Monitor vacancies                    |  Venues/officials availability and  match info |  High  | Allocate venues/officials     |
| Center Manager            |    Monitor activity & usage             |  Reliable reports & operation costs            | Medium | View & export reports         |
| Data Protection Officer   |    Ensure appropriate data processing   |  Privacy retention & role access               |  High  | Review requirements & evidence|
<br/>

## Functional Requirements

| ID | Functional Requirement | Priority |  Source |
| ----------- | ----------- | ----------- | ----------- |
| FR01 |    The system shall authorize reception staff to register a new club                                          |  Must    |  Reception staff |
| FR02 |    The system shall allow an active Club view available matches for a selected date &  time                   |  Must    |      Club        |
| FR03 |    The system shall prevent two confirmed matches from occupying the same facility during overlapping periods |  Must    |   Coordinator    | 
| FR04 |    The system shall allow an active club to book an available venue                                           |  Must    |      Club        |
| FR05 |    The system shall allow an active club to cancel a future match subject to cancellation policy              |  Must    |      Club        |
| FR06 |    The system shall place league-registration requests on a waiting list when the league has reached capacity |  Should  |  Reception Staff |
| FR07 |    The system shall record the team, venue, start time, end time and status for each booking                  |  Must    |  Reception Staff | 
| FR08 |    The system shall allow the manager to generate a venue-usage report for a selected range                   |  Could   |  Center Manager  | 
<br/>

## Rules, Assumptions, Constraints and Risks

| Type | Statement |
| ----------- | ----------- |
| Business Rule  |  A venue may not exceed its approved capacity      |
| Business Rule	 |                                                    |
| Business Rule  |                                                    |
| Business Rule  |                                                    |
| Assumption     | Every unique player has a unique membership number |
| Assumption     | Reception staff have supported web browsers        |
| Constraint     | Existing membership records must be imported       |
| Risk           | Existing spreadsheets may contain duplicates       |
<br/>