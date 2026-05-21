# Smoke Test Checklist — TaskFlow

**Purpose:** Quick validation that core features work after deployment.  
**Duration:** ~15 minutes  
**When:** After every deployment to staging/production.

---

| # | Area | Check | Pass/Fail |
|---|------|-------|-----------|
| 1 | **App Load** | Application loads without errors | ☐ |
| 2 | **App Load** | Login page is displayed correctly | ☐ |
| 3 | **Registration** | New user can register with valid data | ☐ |
| 4 | **Login** | Existing user can log in | ☐ |
| 5 | **Login** | Invalid credentials show error message | ☐ |
| 6 | **Dashboard** | Dashboard loads after login | ☐ |
| 7 | **Dashboard** | Task list is displayed | ☐ |
| 8 | **Create Task** | User can create a new task | ☐ |
| 9 | **Create Task** | Created task appears in the list | ☐ |
| 10 | **Edit Task** | User can edit an existing task | ☐ |
| 11 | **Delete Task** | User can delete a task | ☐ |
| 12 | **Status Change** | Task status can be changed | ☐ |
| 13 | **Filters** | Filters return correct results | ☐ |
| 14 | **Profile** | User profile page loads | ☐ |
| 15 | **Logout** | User can log out | ☐ |
| 16 | **Logout** | After logout, dashboard is not accessible | ☐ |

---

**Result:** ______ / 16 passed  
**Tested by:** _______________  
**Date:** _______________  
**Build:** _______________
