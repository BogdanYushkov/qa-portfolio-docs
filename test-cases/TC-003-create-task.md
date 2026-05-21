# TC-003: Create Task

**Module:** Task Management  
**Priority:** High  
**Preconditions:** User is logged in

---

## TC-003.1: Create task with all fields filled

| Field | Value |
|-------|-------|
| **Steps** | 1. Click "+ New Task" button |
|  | 2. Enter "Write unit tests" in the Title field |
|  | 3. Enter "Cover auth module with Jest tests" in the Description field |
|  | 4. Select priority "High" |
|  | 5. Set due date to tomorrow |
|  | 6. Click "Create" |
| **Expected Result** | Task is created and appears in the task list with status "To Do". All entered data is displayed correctly. Success notification: "Task created successfully." |

---

## TC-003.2: Create task with only required fields

| Field | Value |
|-------|-------|
| **Steps** | 1. Click "+ New Task" button |
|  | 2. Enter "Quick task" in the Title field |
|  | 3. Leave Description, Priority, and Due Date empty |
|  | 4. Click "Create" |
| **Expected Result** | Task is created with default priority "Medium" and no due date. Status is "To Do". |

---

## TC-003.3: Create task with empty title

| Field | Value |
|-------|-------|
| **Steps** | 1. Click "+ New Task" button |
|  | 2. Leave the Title field empty |
|  | 3. Click "Create" |
| **Expected Result** | Validation error: "Title is required." Task is not created. |

---

## TC-003.4: Create task with title exceeding max length

| Field | Value |
|-------|-------|
| **Steps** | 1. Click "+ New Task" button |
|  | 2. Enter a 256-character string in the Title field (max: 255) |
|  | 3. Click "Create" |
| **Expected Result** | Validation error: "Title must not exceed 255 characters." |

---

## TC-003.5: Create task with past due date

| Field | Value |
|-------|-------|
| **Steps** | 1. Click "+ New Task" button |
|  | 2. Enter "Overdue task" in the Title field |
|  | 3. Set due date to yesterday |
|  | 4. Click "Create" |
| **Expected Result** | Validation error: "Due date cannot be in the past." |

---

## TC-003.6: Verify task appears in the list after creation

| Field | Value |
|-------|-------|
| **Steps** | 1. Create a task with title "New feature" |
|  | 2. Navigate to the task list |
| **Expected Result** | Task "New feature" is visible in the list with correct priority, status, and due date. |
