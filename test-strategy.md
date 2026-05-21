# Test Strategy — TaskFlow

## 1. Overview

This document defines the testing strategy for TaskFlow, including testing levels, types, tools, and processes used throughout the project lifecycle.

## 2. Testing Levels

### 2.1 Unit Testing

- **Owner:** Development team
- **Tools:** Jest
- **Coverage target:** ≥ 80% of business logic
- **Scope:** Individual functions, utilities, data validation

### 2.2 Integration Testing

- **Owner:** QA Engineer
- **Tools:** Postman, Newman (CI)
- **Scope:** REST API endpoints, database interactions, authentication flow
- **Approach:** Test each API endpoint with valid/invalid inputs, verify response codes, body, and headers

### 2.3 System Testing

- **Owner:** QA Engineer
- **Tools:** Playwright
- **Scope:** End-to-end user scenarios across the full application
- **Approach:** Simulate real user workflows in supported browsers

### 2.4 Acceptance Testing

- **Owner:** Product Owner + QA
- **Tools:** Manual testing
- **Scope:** Verify business requirements and user stories
- **Approach:** Exploratory testing sessions based on acceptance criteria

## 3. Testing Types

| Type | When | Method |
|------|------|--------|
| Functional | Every sprint | Automated + manual |
| Regression | After bug fixes, before release | Automated suite |
| Smoke | After each deployment | Automated checklist |
| Exploratory | Mid-sprint, pre-release | Manual sessions |
| Usability | Pre-release | Manual review |
| API | Every sprint | Postman collections |

## 4. Test Design Techniques

- **Equivalence Partitioning** — divide inputs into valid/invalid classes
- **Boundary Value Analysis** — test at edges of input ranges
- **Decision Table** — complex business rules (e.g., task status transitions)
- **State Transition** — task lifecycle (To Do → In Progress → Done)
- **Error Guessing** — based on common defect patterns

## 5. Defect Management

### Severity Levels

| Severity | Definition | Example |
|----------|------------|---------|
| Critical | System crash, data loss, security vulnerability | Cannot login, data corruption |
| High | Major feature broken, no workaround | Cannot create tasks |
| Medium | Feature works incorrectly, workaround exists | Filter returns wrong results |
| Low | Minor issue, cosmetic | Typo in label, alignment issue |

### Priority Levels

| Priority | Definition |
|----------|------------|
| P1 — Urgent | Fix immediately, blocks release |
| P2 — High | Fix in current sprint |
| P3 — Medium | Fix in next sprint |
| P4 — Low | Fix when convenient |

### Defect Lifecycle

```
New → Open → In Progress → Fixed → Verified → Closed
                                  → Reopened → In Progress
         → Rejected / Duplicate
```

## 6. Tools

| Purpose | Tool |
|---------|------|
| Test Management | TestRail |
| Bug Tracking | Jira |
| API Testing | Postman |
| UI Automation | Playwright |
| CI/CD | GitHub Actions |
| Test Reporting | Allure |
| Version Control | Git / GitHub |

## 7. CI/CD Integration

- Smoke tests run on every push to `main`
- Full regression suite runs nightly
- API tests run on every pull request
- Test results published to Allure dashboard

## 8. Reporting

| Report | Frequency | Audience |
|--------|-----------|----------|
| Daily Test Execution | Daily | QA Team |
| Sprint Test Summary | End of sprint | Dev Team, PO |
| Release Test Report | Before release | Stakeholders |
| Defect Metrics | Weekly | QA Lead, PM |
