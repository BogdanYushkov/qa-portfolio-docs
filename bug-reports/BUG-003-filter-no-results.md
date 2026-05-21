# BUG-003: Filter shows blank page instead of empty state message

| Field | Value |
|-------|-------|
| **ID** | BUG-003 |
| **Title** | Filter shows blank page instead of empty state message |
| **Severity** | Low |
| **Priority** | P3 — Medium |
| **Status** | Open |
| **Module** | Filtering & Sorting |
| **Environment** | Chrome 120, Windows 11, Production build v1.0.0-rc.1 |
| **Reporter** | QA Engineer |
| **Assigned To** | Frontend Developer |
| **Date** | 2025-01-18 |

## Description

When applying filters that match no tasks, the page displays a blank area instead of the expected "No tasks found" message.

## Steps to Reproduce

1. Log in to the application
2. Navigate to the task list
3. Apply filter: Status = "Done" (when no completed tasks exist)

## Expected Result

Empty state message: "No tasks found matching your filters." with a "Clear Filters" button.

## Actual Result

The task list area is completely blank. No message, no "Clear Filters" button. The user has no indication whether the filter is active or the page failed to load.

## Notes

Minor usability issue. Users may think the application is broken when no results are found. The empty state component exists in the codebase (`EmptyState.tsx`) but is not rendered when the filtered list is empty.
