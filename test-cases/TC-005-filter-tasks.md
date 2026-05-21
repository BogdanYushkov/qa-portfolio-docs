# TC-005: Filter and Sort Tasks

**Module:** Filtering & Sorting  
**Priority:** Medium  
**Preconditions:** User is logged in, multiple tasks exist with different statuses, priorities, and due dates

---

## TC-005.1: Filter by status

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to the task list |
|  | 2. Select filter: Status = "In Progress" |
| **Expected Result** | Only tasks with status "In Progress" are displayed. Task count updates accordingly. |

---

## TC-005.2: Filter by priority

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to the task list |
|  | 2. Select filter: Priority = "High" |
| **Expected Result** | Only tasks with priority "High" are displayed. |

---

## TC-005.3: Combine multiple filters

| Field | Value |
|-------|-------|
| **Steps** | 1. Select filter: Status = "To Do" |
|  | 2. Add filter: Priority = "Critical" |
| **Expected Result** | Only tasks matching both criteria are shown. |

---

## TC-005.4: Sort by due date ascending

| Field | Value |
|-------|-------|
| **Steps** | 1. Click "Due Date" column header |
| **Expected Result** | Tasks are sorted with the earliest due date first. Tasks without a due date appear at the end. |

---

## TC-005.5: Sort by priority descending

| Field | Value |
|-------|-------|
| **Steps** | 1. Click "Priority" column header to sort descending |
| **Expected Result** | Tasks are sorted: Critical → High → Medium → Low. |

---

## TC-005.6: Clear all filters

| Field | Value |
|-------|-------|
| **Precondition** | Filters are applied |
| **Steps** | 1. Click "Clear Filters" button |
| **Expected Result** | All filters are removed. Full task list is displayed. |

---

## TC-005.7: Filter with no matching results

| Field | Value |
|-------|-------|
| **Precondition** | No tasks with status "Done" exist |
| **Steps** | 1. Select filter: Status = "Done" |
| **Expected Result** | Empty state message: "No tasks found matching your filters." |
