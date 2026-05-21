# Requirements Traceability Matrix — TaskFlow

A traceability matrix links each business requirement to its corresponding test cases. It helps ensure that every requirement is tested (coverage) and that no tests exist without a matching requirement (relevance). Read it row by row: each row shows a requirement and which test cases verify it.

## Legend

- **REQ**: Requirement ID
- **TC**: Test Case ID
- **Status**: Covered / Partially Covered / Not Covered

---

## Authentication

| REQ ID | Requirement | Test Cases | Status |
|--------|------------|------------|--------|
| REQ-001 | User can register with email and password | TC-001.1, TC-001.2, TC-001.3, TC-001.4, TC-001.5, TC-001.6 | Covered |
| REQ-002 | System validates email format | TC-001.3 | Covered |
| REQ-003 | Password must meet security policy (8+ chars, upper, lower, number, special) | TC-001.4 | Covered |
| REQ-004 | System prevents duplicate email registration | TC-001.2 | Covered |
| REQ-005 | User can log in with valid credentials | TC-002.1 | Covered |
| REQ-006 | System shows generic error for invalid login | TC-002.2, TC-002.3 | Covered |
| REQ-007 | User can log out | TC-002.5 | Covered |
| REQ-008 | Session persists across page refresh | TC-002.6 | Covered |

## Task Management

| REQ ID | Requirement | Test Cases | Status |
|--------|------------|------------|--------|
| REQ-009 | User can create a task with title, description, priority, due date | TC-003.1, TC-003.2 | Covered |
| REQ-010 | Task title is required | TC-003.3 | Covered |
| REQ-011 | Task title max length is 255 characters | TC-003.4 | Covered |
| REQ-012 | Due date cannot be in the past | TC-003.5 | Covered |
| REQ-013 | Default task priority is Medium | TC-003.2 | Covered |
| REQ-014 | Default task status is To Do | TC-003.1, TC-003.2 | Covered |
| REQ-015 | User can edit task properties | TC-004.1, TC-004.2, TC-004.3 | Covered |
| REQ-016 | User can delete a task | TC-004.4 | Covered |
| REQ-017 | Task status flow: To Do → In Progress → Done | TC-004.6 | Covered |

## Filtering & Sorting

| REQ ID | Requirement | Test Cases | Status |
|--------|------------|------------|--------|
| REQ-018 | User can filter tasks by status | TC-005.1 | Covered |
| REQ-019 | User can filter tasks by priority | TC-005.2 | Covered |
| REQ-020 | Filters can be combined | TC-005.3 | Covered |
| REQ-021 | User can sort tasks by due date | TC-005.4 | Covered |
| REQ-022 | User can sort tasks by priority | TC-005.5 | Covered |
| REQ-023 | User can clear all filters | TC-005.6 | Covered |
| REQ-024 | Empty filter results show appropriate message | TC-005.7 | Covered |

## User Profile

| REQ ID | Requirement | Test Cases | Status |
|--------|------------|------------|--------|
| REQ-025 | User can view their profile | — | Not Covered |
| REQ-026 | User can edit their name | — | Not Covered |
| REQ-027 | User can change their password | — | Not Covered |

---

## Coverage Summary

| Category | Total Requirements | Covered | Not Covered | Coverage |
|----------|--------------------|---------|-------------|----------|
| Authentication | 8 | 8 | 0 | 100% |
| Task Management | 9 | 9 | 0 | 100% |
| Filtering & Sorting | 7 | 7 | 0 | 100% |
| User Profile | 3 | 0 | 3 | 0% |
| **Total** | **27** | **24** | **3** | **89%** |
