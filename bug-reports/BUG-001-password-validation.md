# BUG-001: Password validation accepts passwords without special characters

| Field | Value |
|-------|-------|
| **ID** | BUG-001 |
| **Title** | Password validation accepts passwords without special characters |
| **Severity** | High |
| **Priority** | P2 — High |
| **Status** | Open |
| **Module** | Authentication — Registration |
| **Environment** | Chrome 120, Windows 11, Production build v1.0.0-rc.1 |
| **Reporter** | QA Engineer |
| **Assigned To** | Backend Developer |
| **Date** | 2025-01-16 |

## Description

The registration form accepts passwords that do not contain special characters, violating the password policy defined in the requirements.

## Steps to Reproduce

1. Navigate to `/register`
2. Fill in First Name, Last Name, and Email with valid data
3. Enter `SecurePass123` in the Password field (no special character)
4. Enter `SecurePass123` in the Confirm Password field
5. Click "Sign Up"

## Expected Result

Validation error: "Password must include at least one special character (!@#$%^&*)."

## Actual Result

Registration succeeds. User is created with a password that does not meet the security policy.

## Attachments

- Screenshot: registration success with weak password
- Console log: no validation errors

## Notes

Users can create accounts with weak passwords, increasing the risk of brute-force attacks. Violates security requirements SEC-001. Frontend validation is missing the special character check. Backend API also does not enforce this rule — both need to be fixed.
