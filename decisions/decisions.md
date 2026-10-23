# Decision Log

This log explains the main choices considered during the analysis. Items marked Proposed still need to be checked against the original scenario.

## D01 — Keep venue allocations separate from fixtures

**Status:** Proposed.

**Decision:** Use VenueAllocation to record a fixture's proposed or confirmed venue booking.

**Related requirements:** FR03, FR04 and FR09.

**Other option:** Store the venue directly in Fixture without a separate allocation.

**Reason:** A proposed booking is different from a confirmed booking. Keeping allocations separate makes their status clearer.

**Still to check:** Does a provisional booking stop others from booking the venue? Should previous allocations be kept? The fixture and allocation times must also agree.

## D02 — Keep unallocated requests separate from fixtures

**Status:** Proposed.

**Decision:** Use FixtureRequest to record requests that have not yet been arranged, including why they remain unallocated.

**Related requirement:** FR06.

**Other option:** Record every request as an unconfirmed fixture.

**Reason:** A request may not have agreed teams, times or a venue. Keeping it separate avoids treating it as an arranged fixture.

**Still to check:** Who submits requests? What information must they provide? Can one request lead to several fixtures? The current model assumes a request can lead to no more than one fixture.

## D03 — Keep match officials and appointments in scope

**Status:** Proposed — supporting requirements are still needed.

**Decision:** Keep MatchOfficial and OfficialAppointment in the domain model.

**Basis:** The report includes officials and appointments in its purpose, scope and fixture-allocation use case.

**Other option:** Leave official appointments outside the initial system.

**Reason:** Removing them from the diagram would conflict with the report. The original scenario should determine whether they stay in scope.

**Still to check:** Add requirements and use cases if appointments remain in scope. Also clarify how official availability and suitability are recorded.

## D04 — Generate reports from existing information

**Status:** Proposed.

**Decision:** Do not add a separate Report class just for venue-usage reporting.

**Related requirement:** FR08.

**Other option:** Add a VenueUsageReport class.

**Reason:** The system can produce the report using information already held about venues, fixtures and allocations.

**Still to check:** Does venue usage mean confirmed bookings, completed fixtures or provisional bookings? A separate report class may be useful if reports need their own approval or version history.

## D05 — Separate the current result from correction history

**Status:** Proposed — correction history needs clarification.

**Decision:** Store one current Result for each fixture, including its scores, status, recording time and who recorded it.

**Related requirement:** FR10.

**Other option:** Keep separate records of every result change and correction decision.

**Reason:** One current result meets the basic recording requirement. It does not keep previous scores or explain corrections.

**Still to check:** Confirm the required result format. If previous values and correction reasons must be kept, update the requirements and model to include them.

## D06 — Check rules before treating them as confirmed

**Status:** Proposed — evidence needs checking.

**Decision:** Check the drafted rules against the original scenario.

**Basis:** BR01–BR04 describe capacity limits, age eligibility, prior experience and suspended teams. The report also mentions imports, travel checks and approvals.

**Other option:** Treat every drafted statement as an established league rule.

**Reason:** The brief asks for clear differences between known facts, assumptions and unanswered questions.

**Still to check:** Add evidence for each rule or record a clarification question. Explain what counts towards venue capacity, how age is checked, what experience is required and who can approve decisions.

## D07 — Check and declare AI assistance

**Status:** AI was used.

**What happened:** AI suggested use-case diagrams and several domain-model drafts. One draft removed official appointments to match the requirements table. A later draft restored them because they remained in the report's scope.

**What this showed:** The report, requirements, use cases and diagrams must be checked together. Matching one document is not enough.

**Next steps:** Keep examples of the AI interactions. Explain which suggestions were checked, changed or rejected, and why. Clearly identify AI assistance and make sure the final choices reflect the student's own understanding.
