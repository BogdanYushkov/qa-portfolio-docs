# TC-004: Edit Task

**Module:** Task Management  
**Priority:** High  
**Preconditions:** User is logged in, at least one task exists

---

## TC-004.1: Edit task title

| Field | Value |
|-------|-------|
| **Steps** | 1. Click on an existing task to open it |
|  | 2. Click "Edit" |
|  | 3. Change the title to "Updated task title" |
|  | 4. Click "Save" |
| **Expected Result** | Task title is updated. Success notification: "Task updated." Updated title is displayed in the task list. |

---

## TC-004.2: Change task status

| Field | Value |
|-------|-------|
| **Steps** | 1. Open a task with status "To Do" |
|  | 2. Change status to "In Progress" |
|  | 3. Click "Save" |
| **Expected Result** | Task status is updated to "In Progress". Task moves to the correct column/section in the list. |

---

## TC-004.3: Change task priority

| Field | Value |
|-------|-------|
| **Steps** | 1. Open a task with priority "Medium" |
|  | 2. Change priority to "Critical" |
|  | 3. Click "Save" |
| **Expected Result** | Task priority is updated. Priority badge/indicator changes to "Critical". |

---

## TC-004.4: Delete a task

| Field | Value |
|-------|-------|
| **Steps** | 1. Open an existing task |
|  | 2. Click "Delete" |
|  | 3. Confirm deletion in the dialog |
| **Expected Result** | Task is removed from the list. Success notification: "Task deleted." Task is no longer accessible. |

---

## TC-004.5: Cancel editing without saving

| Field | Value |
|-------|-------|
| **Steps** | 1. Open a task and click "Edit" |
|  | 2. Change the title |
|  | 3. Click "Cancel" |
| **Expected Result** | Changes are discarded. Original task data is preserved. |

---

## TC-004.6: Complete task lifecycle

| Field | Value |
|-------|-------|
| **Steps** | 1. Create a new task |
|  | 2. Change status from "To Do" to "In Progress" |
|  | 3. Change status from "In Progress" to "Done" |
| **Expected Result** | Task moves through all statuses correctly. Status history is maintained. "Done" status is visually distinct (e.g., strikethrough or green indicator). |
