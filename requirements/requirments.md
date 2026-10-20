# Requirements & Buisness Rules 

## Classify Statements 
| Statement | Classification | Reason | 
| ----------- | ----------- | ----------- | 
| Fixture details are copied into different spreadsheets       | Problem evidence | Describes the current situation of fragmentation data management |  
| A venue must not exceed the approved capacity                | Business Rule    | An organizational policy which must always be enforced           |  
| The initial service must be accessible through a web browser | Constraint       | Restricts how the solution may be delivered                      |  
| Existing club records may contain duplicate contact details  | Risk             | Uncertainty may negatively affect implementation                 |   
| Every club has access to an email                            | Assumption       | Believed to be true but requires verification                    |   
<br>


## Functional Requirements

| ID | Functional Requirement | Priority |  Source |
| ----------- | ----------- | ----------- | ----------- |
| FR01 |    The system shall authorize league staff to register a new club                                             |  Must    |   League staff   |
| FR02 |    The system shall allow an active Club view available matches for a selected date &  time                   |  Must    |      Club        |
| FR03 |    The system shall prevent two confirmed matches from occupying the same facility during overlapping periods |  Must    |   Coordinator    | 
| FR04 |    The system shall allow the coordinator to provisionally allocate a venue                                   |  Must    |   Coordinator    |
| FR05 |    The system shall record fixture postponements or cancellations, their reasons and the decision status      |  Must    |   League staff   |
| FR06 |    The system shall ecording unallocated requests and why they remain unallocated                             |  Should  |   League Staff   |
| FR07 |    The system shall record the team, venue, start time, end time and status for each fixture                  |  Must    |   League Staff   | 
| FR08 |    The system shall allow the manager to generate a venue-usage report for a selected date range              |  Could   |  League Manager  | 
<br>

## Use-Case Catalogue

| ID | Candidate Use Case | Primary Actor | Related Requirement |
| --- | --- | --- | --- |
| UC01 | Register a club                             | League Staff             | FR01 |
| UC02 | View available matches                      | Club                     | FR02 |
| UC03 | Provisionally allocate a venue              | Coordinator              | FR04 |
| UC04 | Record fixture postponement or cancellation | League Staff             | FR05 |
| UC05 | Record an unallocated request               | League Staff             | FR06 |
| UC06 | Maintain fixture details                    | League Staff             | FR07 |
| UC07 | Generate a venue-usage report               | League Manager           | FR08 |



## Non-Functional Requirements

| ID | Quality Category | Measurable Requirment | 
| ----------- | ----------- | ----------- |
| NFR01 | Performance   | Venue-availability results shall be displayed within three seconds for at least 95% of requests under normal operating conditions  |
| NFR02 | Security      | Players contact and emergency information will only be available to authenticated users with authorised permissions                |
| NFR03 | Availability  | The system shall be available during league operating hours excluding scheduled maintenance announced at least 24 hours in advance | 
| NFR04 | Accessability | All participant registration functions shall be operable using a keyboard-only navigation                                          |
<br>


## Business Rules

| ID | Business Rule |
| --- | --- |
| BR01 | A venue may not exceed its approved capacity                                   |
| BR02 | Players must satisfy any age requirements before registration                  |
| BR03 | The league requires some proof of prior experience before a club is accepted   |
| BR04 | A suspended team cannot book a new fixture                                     |
