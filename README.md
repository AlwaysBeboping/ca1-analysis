# CA1: Individual Requirments and Domain Analysis By Kieran Stack

**CA1 Scenario 26: Youth Sports League Coordination Service**

## Table Of Contents

| Document | Section |
| --- | --- |
| Scenario analysis | [Business problem statement](report/report.md#business-problem-statement) |
| Scenario analysis | [Purpose statement](report/report.md#purpose-statement) |
| Scenario analysis | [Scope](report/report.md#scope) |
| Scenario analysis | [Stakeholder analysis](report/report.md#stakeholder-analysis) |
| Scenario analysis | [Actor catalogue](report/report.md#actor-and-stakeholder-catalogue) |
| Scenario analysis | [Rules and uncertainty](report/report.md#rules-assumptions-constraints-and-risks) |
| Scenario analysis | [Clarification questions](report/report.md#stakeholder-clarification-questions) |
| Scenario analysis | [Use Case Models](report/report.md##use-case-model) |
| Requirements | [Classify Statements](requirements/requirments.md#classify-statements) |
| Requirements | [Functional requirements](requirements/requirments.md#functional-requirements) |
| Requirements | [Use Case Catalogue](requirements/requirments.md#Use-case-catalogue) |
| Requirements | [Non-functional requirements](requirements/requirments.md#non-functional-requirements) |
| Requirements | [Buisness Rules](requirements/requirments.md#buisness-rules) |
| Diagrams | [Club Use Cases](diagrams/club-use-cases.puml) |
| Diagrams | [Coorinator Use Cases](diagrams/coorinator-use-cases.puml) |
| Diagrams | [Staff Use Cases](diagrams/staff-use-cases.puml) |
| Diagrams | [Domain Model](diagrams/domain-model.puml)|


## Scenario CA1-26-YSLC

**How to use this scenario** This document provides the case evidence for your assigned CA1 analysis. Complete the work and submission described in the main CA1 specification. Where evidence is incomplete or inconsistent, identify the uncertainty rather than inventing a confirmed policy.

## Organisation and current service

Kerry Youth Sports League coordinates teams, fixtures, venues, officials and results across several age-group competitions.

Team entries, player eligibility, venue availability, official appointments and schedule changes are managed through forms, spreadsheets and messages.

## Requests, eligibility and preparation

Clubs enter teams and provide contacts, home venues and eligibility information. Entries can remain incomplete while fixture planning has already begun.

Requests arrive through several channels and may be incomplete. Staff need to distinguish an initial expression of interest, a request awaiting evidence and a request ready for a decision. Priorities and exceptions are not applied consistently.

Another person or organisation may assist with a request. Staff are uncertain what authority is required before detailed information or decisions can be shared.

## Allocation and coordination

Fixture planning must combine competition rules, team availability, venue capacity, travel and officials. Postponing one fixture can affect later rounds and shared resources.

Capacity depends on a combination of people, places, resources and timing. A visible vacancy does not necessarily mean that every requirement is satisfied. Provisional allocations sometimes remain in place while essential information is still missing.

Changes can affect several linked arrangements. Staff need to preserve the current confirmed position while retaining evidence of earlier decisions and versions.

## Progress, review and exceptions

Staff record progress, decisions and outstanding actions using notes, messages and spreadsheets. Different teams use status terms differently, making it difficult to identify what is awaiting action and who is responsible.

A planned activity may be changed, partially completed, paused or withdrawn. Staff need to distinguish an operational change from a formal decision and avoid treating silence as approval.

Reviews may generate new actions, revised arrangements or escalation. Earlier evidence should not be overwritten when circumstances change.

## Information, reporting and scope

The coordinator needs information about unallocated requests, provisional arrangements, capacity conflicts, overdue actions and incomplete records. External partners should receive only the information required for their role.

Summary reporting is needed for management and funders without exposing unnecessary personal or commercially sensitive information. Connectivity may be unreliable during off-site work.

The initial scope covers service coordination and records. Specialist professional systems, financial accounting and unrelated public website functions are outside scope.

## Stakeholder evidence

- Coordinator: "A vacancy is not a match unless all of the important requirements are satisfied."
- Service user: "I need to know whether I am waiting for information, a decision or an outside organisation."
- Administrator: "Provisional arrangements can block capacity long after the original request has stalled."
- Partner representative: "I need the information required for my role, not the complete case history."
- Reviewer: "New information should be added without erasing the basis of the earlier decision."
- Manager: "We need consistent reasons for delay, withdrawal and incomplete outcomes."

## Unresolved matters

The scenario does not confirm every policy or decision. Clarification may be required about:

- what information is required before a request is ready for decision;
- how eligibility, priority and exceptions should be applied;
- what authority is required when another person acts for the requester;
- when provisional allocations should expire or become confirmed;
- who may approve changes, substitutions or withdrawal;
- how versions, reviews and outstanding actions should be related;
- which information may be shared with staff, partners and funders.

**Important** Use scenario evidence, state temporary assumptions clearly, and identify questions or risks where stakeholder confirmation is required.

# Scenario: Youth Sports League Coordination Service Summary

Kerry Youth Sports Center League currently coordinates teams, fixtures, venues, officials and results across several age groups competitions. Booking requests arrive by telephone, email and at the reception desk. Staff sometimes receive conflicting requests for the same clubs, venues and officials. Clubs must contact reception to check availability and fixtures are maintained manually. Management cannot easily determine venue usage, team and official availability. The league wants to improve the accuracy and accessibility of this information.
