# TC-001: User Registration

**Module:** Authentication  
**Priority:** High  
**Preconditions:** User is not logged in, registration page is open

---

## TC-001.1: Successful registration with valid data

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/register` |
|  | 2. Enter "John" in the First Name field |
|  | 3. Enter "Doe" in the Last Name field |
|  | 4. Enter "john.doe@example.com" in the Email field |
|  | 5. Enter "SecurePass123!" in the Password field |
|  | 6. Enter "SecurePass123!" in the Confirm Password field |
|  | 7. Click the "Sign Up" button |
| **Expected Result** | User is registered and redirected to the dashboard. Welcome message "Hello, John!" is displayed. |

---

## TC-001.2: Registration with already registered email

| Field | Value |
|-------|-------|
| **Precondition** | Email "john.doe@example.com" is already registered |
| **Steps** | 1. Navigate to `/register` |
|  | 2. Fill in all fields with valid data using email "john.doe@example.com" |
|  | 3. Click "Sign Up" |
| **Expected Result** | Error message: "This email is already registered. Please log in or use a different email." User remains on the registration page. |

---

## TC-001.3: Registration with invalid email format

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/register` |
|  | 2. Enter "john.doe" in the Email field |
|  | 3. Click "Sign Up" |
| **Expected Result** | Validation error: "Please enter a valid email address." |

---

## TC-001.4: Registration with weak password

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/register` |
|  | 2. Enter "123" in the Password field |
|  | 3. Click "Sign Up" |
| **Expected Result** | Validation error: "Password must be at least 8 characters and include uppercase, lowercase, number, and special character." |

---

## TC-001.5: Registration with mismatched passwords

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/register` |
|  | 2. Enter "SecurePass123!" in Password |
|  | 3. Enter "DifferentPass456!" in Confirm Password |
|  | 4. Click "Sign Up" |
| **Expected Result** | Validation error: "Passwords do not match." |

---

## TC-001.6: Registration with empty required fields

| Field | Value |
|-------|-------|
| **Steps** | 1. Navigate to `/register` |
|  | 2. Leave all fields empty |
|  | 3. Click "Sign Up" |
| **Expected Result** | Validation errors shown for all required fields: First Name, Last Name, Email, Password. |
