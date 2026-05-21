# Regression Test Checklist — TaskFlow

**Purpose:** Comprehensive validation of all features before release.  
**Duration:** ~2 hours  
**When:** Before each release, after significant bug fixes.

---

## Authentication

| # | Check | Pass/Fail |
|---|-------|-----------|
| 1 | Register with valid data | ☐ |
| 2 | Register with duplicate email — error shown | ☐ |
| 3 | Register with invalid email — validation error | ☐ |
| 4 | Register with weak password — validation error | ☐ |
| 5 | Register with mismatched passwords — validation error | ☐ |
| 6 | Register with empty fields — all validations fire | ☐ |
| 7 | Login with valid credentials | ☐ |
| 8 | Login with wrong password — error shown | ☐ |
| 9 | Login with unregistered email — error shown | ☐ |
| 10 | Login with empty fields — validation error | ☐ |
| 11 | Logout — session terminated | ☐ |
| 12 | Session persists after page refresh | ☐ |
| 13 | Protected pages redirect to login when not authenticated | ☐ |

## Task Management

| # | Check | Pass/Fail |
|---|-------|-----------|
| 14 | Create task with all fields | ☐ |
| 15 | Create task with required fields only | ☐ |
| 16 | Create task without title — validation error | ☐ |
| 17 | Create task with title exceeding max length — validation error | ☐ |
| 18 | Create task with past due date — validation error | ☐ |
| 19 | Edit task title | ☐ |
| 20 | Edit task description | ☐ |
| 21 | Change task priority | ☐ |
| 22 | Change task status: To Do → In Progress | ☐ |
| 23 | Change task status: In Progress → Done | ☐ |
| 24 | Delete task with confirmation | ☐ |
| 25 | Cancel task editing — changes discarded | ☐ |
| 26 | Task data persists after page refresh | ☐ |

## Filtering & Sorting

| # | Check | Pass/Fail |
|---|-------|-----------|
| 27 | Filter by status | ☐ |
| 28 | Filter by priority | ☐ |
| 29 | Combine multiple filters | ☐ |
| 30 | Sort by due date | ☐ |
| 31 | Sort by priority | ☐ |
| 32 | Clear all filters | ☐ |
| 33 | Filter with no results — empty state shown | ☐ |

## User Profile

| # | Check | Pass/Fail |
|---|-------|-----------|
| 34 | View profile page | ☐ |
| 35 | Edit profile — name updated | ☐ |
| 36 | Change password — old password required | ☐ |
| 37 | Change password — new password policy enforced | ☐ |

## Cross-Browser

| # | Check | Pass/Fail |
|---|-------|-----------|
| 38 | Chrome — core flow works | ☐ |
| 39 | Firefox — core flow works | ☐ |
| 40 | Safari — core flow works | ☐ |

---

**Result:** ______ / 40 passed  
**Tested by:** _______________  
**Date:** _______________  
**Build:** _______________  
**Notes:**
