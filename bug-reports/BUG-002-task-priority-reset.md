# BUG-002: Task priority resets to Medium after editing description

| Field | Value |
|-------|-------|
| **ID** | BUG-002 |
| **Title** | Task priority resets to Medium after editing description |
| **Severity** | Medium |
| **Priority** | P2 — High |
| **Status** | Open |
| **Module** | Task Management — Edit |
| **Environment** | Firefox 121, macOS 14.2, Production build v1.0.0-rc.1 |
| **Reporter** | QA Engineer |
| **Assigned To** | Frontend Developer |
| **Date** | 2025-01-17 |

## Description

When a user edits only the task description and saves, the task priority is silently reset to "Medium" regardless of its previous value.

## Steps to Reproduce

1. Log in and create a task with priority "Critical"
2. Open the task and click "Edit"
3. Modify the description text (do not change priority)
4. Click "Save"
5. Observe the task priority

## Expected Result

Task priority remains "Critical". Only the description is updated.

## Actual Result

Task priority changes from "Critical" to "Medium". No warning or notification about the change.

## Notes

Users lose priority settings when editing tasks. Critical tasks may be deprioritized without notice, affecting team workflow. Suspected root cause: the edit form initializes the priority dropdown with the default value "Medium" instead of the current task priority.
