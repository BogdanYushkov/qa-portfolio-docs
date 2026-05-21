# TC-002: Login

**Module:** Authentication  
**Priority:** High  
**Preconditions:** User with email "john.doe@example.com" and password "SecurePass123!" exists

---

## TC-002.1: Successful login with valid credentials

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/login` |
|  | 2. Enter "john.doe@example.com" in the Email field |
|  | 3. Enter "SecurePass123!" in the Password field |
|  | 4. Click "Log In" |
| **Expected Result** | User is redirected to the dashboard. User name is displayed in the header. |

---

## TC-002.2: Login with incorrect password

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/login` |
|  | 2. Enter "john.doe@example.com" in the Email field |
|  | 3. Enter "WrongPassword!" in the Password field |
|  | 4. Click "Log In" |
| **Expected Result** | Error message: "Invalid email or password." User remains on the login page. |

---

## TC-002.3: Login with unregistered email

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/login` |
|  | 2. Enter "unknown@example.com" in the Email field |
|  | 3. Enter "SomePass123!" in the Password field |
|  | 4. Click "Log In" |
| **Expected Result** | Error message: "Invalid email or password." (Same generic message for security.) |

---

## TC-002.4: Login with empty fields

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/login` |
|  | 2. Leave Email and Password fields empty |
|  | 3. Click "Log In" |
| **Expected Result** | Validation errors for Email and Password fields. |

---

## TC-002.5: Logout

| Field | Value |
|-------|-------|
| **Precondition** | User is logged in |
| **Steps** | 1. Click the user avatar/menu in the header |
|  | 2. Click "Log Out" |
| **Expected Result** | User is redirected to the login page. Session is terminated. Accessing `/dashboard` redirects to `/login`. |

---

## TC-002.6: Session persistence after page refresh

| Field | Value |
|-------|-------|
| **Precondition** | User is logged in |
| **Steps** | 1. Refresh the browser page (F5) |
| **Expected Result** | User remains logged in. Dashboard content is displayed correctly. |
