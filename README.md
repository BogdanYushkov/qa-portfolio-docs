# QA Portfolio — Documentation Examples

This repository contains QA documentation examples for **TaskFlow**, a fictional web-based task management application. The documents demonstrate how to structure and write professional QA artifacts.

> **Note:** TaskFlow is not a real application. It is an imaginary project created solely to showcase QA documentation skills and best practices.

## About TaskFlow

TaskFlow is a simple web application for managing personal and team tasks. Core features include:

- User registration and authentication
- Creating, editing, and deleting tasks
- Setting task priority (Low / Medium / High / Critical)
- Task status workflow (To Do → In Progress → Done)
- Filtering and sorting tasks by status, priority, and due date
- User profile management

**Tech stack:** React frontend, Node.js/Express backend, PostgreSQL database.

## Documentation

| Document | Description |
|----------|-------------|
| [Test Plan](test-plan.md) | Overall testing approach, scope, schedule, and resources |
| [Test Strategy](test-strategy.md) | Testing levels, types, tools, and entry/exit criteria |
| [Test Cases](test-cases/) | Detailed test cases for core features |
| [Bug Reports](bug-reports/) | Sample bug reports with severity and priority |
| [Checklists](checklists/) | Smoke and regression checklists |
| [Traceability Matrix](traceability-matrix.md) | Requirements-to-test-cases mapping |

## Structure

```
├── README.md
├── test-plan.md
├── test-strategy.md
├── test-cases/
│   ├── TC-001-user-registration.md
│   ├── TC-002-login.md
│   ├── TC-003-create-task.md
│   ├── TC-004-edit-task.md
│   └── TC-005-filter-tasks.md
├── bug-reports/
│   ├── BUG-001-password-validation.md
│   ├── BUG-002-task-priority-reset.md
│   └── BUG-003-filter-no-results.md
├── checklists/
│   ├── smoke-checklist.md
│   └── regression-checklist.md
└── traceability-matrix.md
```
