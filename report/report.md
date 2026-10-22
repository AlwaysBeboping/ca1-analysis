# Scenario Analysis

## Business Problem Statement
Kerry Youth Sports League uses paper forms, spreadsheets and messages to manage clubs, teams, fixtures, venues, officials and results across several age group competitions. Information is fragmented across several records and communication channels such as paper forms, spreadsheets and phone messages and is entered manually into different spreadsheets by different staff members. Staff cannot reliably prevent conflicting venues/officials/fixtures, teams must contact staff to check availability and fixtures require manual maintenance.

Staff struggle to distinguish initial interest, missing evidence and readiness for a decision. These issues increase administrative effort, reduce confidence in the leagues records and may result in an inconsistent service for clubs. The proposed Sports League Management System will manage clubs and their respective teams  with searchable fixtures, fixture results, available venues, available officials and basic management reporting. Team managers also recieve fixture information in different formats making fixture mangement inefficient and increasing the likelihood for errors.

# Purpose Statement 
The proposed Youth Sports League Management System will support team entries, venue availability, venue bookings, official availability, official appointments, team records, coordinate fixtures and basic operational reporting.

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

## Actor and Stakeholder Catalogue

| Actor or Stakeholder | Type | Goal or Interest | Direct Interaction? |
| --- | --- | --- | --- |
| Club Representative | Primary actor | Register teams and view fixture information | Yes |
| Player | Primary actor, if direct access is provided | View upcoming fixtures and results | Yes, if players access the system directly |
| League Staff | Primary actor | Maintain records, process team entries and record fixture changes | Yes |
| Coordinator | Primary actor | Allocate fixtures, venues and available officials without conflicts | Yes |
| League Manager | Primary actor | Generate and view operational and venue-usage reports | Yes |
| Match Official | Primary actor | Provide availability and view appointments and schedule changes | Yes |
| System Admin | Primary actor | Manage user accounts, permissions and system access | Yes |
| Notification Service | Supporting actor, if external | Deliver fixture and appointment notifications | Yes, if directly called by the system |
| Data Protection Officer | Offstage stakeholder | Ensure appropriate protection, access and retention of personal information | No, unless direct system access is required |
| Funders | Offstage stakeholder | Assess how funding supports the league through summary reports | No, if reports are supplied by league management |

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

## Use-Case Model

### Detailed Use Case — UC-02 Allocate Fixture
## Use Cases

### UC-01 — Register Team

**Primary actor:** Club Representative  
**Goal:** Enter a team into a competition  
**Trigger:** The Club Representative selects the option to register a team

#### Preconditions

- The Club Representative is authenticated and authorised to represent the club
- The competition is open for registration
- The applicable registration and eligibility rules are available

#### Main Flow

1. The Club Representative selects the competition
2. The system requests the required team and club information
3. The Club Representative enters the information and submits the registration
4. The system validates the required information and checks the applicable registration rules
5. The system creates the team registration and assigns its status
6. The system displays confirmation of submission and the registration status

#### Alternative and Exception Flows

- **Missing or invalid information:** The system identifies the affected fields and allows the representative to correct them
- **Duplicate registration:** The system flags an existing registration for the same team and competition and prevents a duplicate submission
- **Eligibility review required:** The system records the registration as pending review by League Staff
- **Registration closed:** The system prevents submission and explains that registration is closed

#### Postconditions

- A successful submission is stored with its registration status
- A registration requiring review remains pending until an explicit decision is recorded
- An unsuccessful submission does not create a completed registration

---

### UC-09 — Allocate Fixture

**Primary actor:** Coordinator  
**Goal:** Arrange a fixture that meets all requirements  
**Trigger:** A competition requires a fixture to be scheduled

#### Preconditions

- The Coordinator is authenticated and authorised to allocate fixtures
- The participating teams are registered and eligible for the competition
- Relevant team availability, venue details and official availability are recorded
- The applicable scheduling requirements are available

#### Main Flow

1. The Coordinator selects the competition and participating teams.
2. The Coordinator proposes a date, time and venue
3. The system checks competition rules, team availability, venue availability and capacity, and travel requirements
4. The Coordinator assigns the required match officials
5. The system checks official availability and suitability
6. The Coordinator records any required explicit approvals
7. The system verifies that all allocation requirements are satisfied
8. The Coordinator confirms the allocation
9. The system saves the fixture as confirmed and displays its details

#### Alternative and Exception Flows

- **Scheduling conflict:** The system identifies the conflicting team, venue or official allocation and allows the Coordinator to revise the proposal
- **Requirements not satisfied:** The system identifies the unmet requirements and prevents confirmation
- **Approval outstanding:** The fixture remains provisional. A lack of response is not treated as approval
- **No suitable allocation available:** The Coordinator saves the proposal as provisional for further review

#### Postconditions

- A confirmed fixture satisfies all applicable allocation requirements
- An unresolved proposal remains clearly marked as provisional
- The allocation details, approvals and decision history are stored

---

### UC-10 — Record Fixture Result

**Primary actor:** League Staff  
**Goal:** Maintain accurate competition results  
**Trigger:** League Staff receive a fixture outcome and select the option to record it

#### Preconditions

- League Staff are authenticated and authorised to record results
- The fixture exists
- The fixture outcome and any required supporting information are available

#### Main Flow

1. League Staff select the fixture.
2. The system displays the participating teams and fixture details
3. League Staff enter the result and any required supporting information
4. The system checks that the information is complete and valid
5. The system displays the entered result for review
6. League Staff confirm the submission
7. The system saves the result against the fixture
8. The system records who entered the result and when

#### Alternative and Exception Flows

- **Missing or invalid information:** The system identifies the problem and requests correction before saving
- **Result already recorded:** The system displays the existing result and directs League Staff to the authorised correction process
- **Conflicting or disputed information:** League Staff record the issue for review; the result is not treated as final until resolved
- **Postponed or abandoned fixture:** League Staff record the applicable fixture status instead of a completed-match score

#### Postconditions

- A valid, confirmed result is stored against the correct fixture
- The entry is traceable to the member of League Staff who recorded it
- Any authorised correction preserves the previous value and the reason for the change
- An unresolved result is clearly identified as awaiting review

---