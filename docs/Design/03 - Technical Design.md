# 03 - Technical Design

## Purpose

This document defines the technical approach that will be used to develop Finance Platform. It establishes the technologies, architecture, development practices and security measures that will be used to implement the proposed solution.

The technical design is intended to keep the Beta version simple and understandable while providing a suitable foundation for future development.

---

# Introduction

The Finance Platform will be developed as a web application using technologies that are familiar to the developer and appropriate for the requirements of the project.

The application will use a straightforward client-server structure. HTML, CSS and JavaScript will form the frontend, PHP will provide the server-side functionality, and MySQL will be used to store the application's data.

The project will initially avoid unnecessary frameworks and complexity. The system will be developed in a simple form first, with refactoring taking place later where improvements are required.

---

# Technology Stack

| Technology | Purpose | Reason for Selection |
|------------|---------|----------------------|
| **HTML** | Structure of webpages and interface elements. | Provides the standard structure required for a web application. |
| **CSS** | Styling, layout and responsive design. | Allows the interface to be designed and adapted for different screen sizes. |
| **JavaScript** | Client-side interaction and data visualisation. | Provides additional interactivity and will be used to create the project's graphs and charts. |
| **PHP** | Server-side application logic and communication with the database. | The developer has existing experience with PHP and it works well with MySQL. |
| **MySQL** | Storage and management of application data. | A relational database is suitable for organising users, assets, liabilities and historical financial information. |
| **Git** | Version control. | Allows changes to the project to be tracked and previous versions to be maintained. |
| **GitHub** | Remote repository and project history. | Provides a central location for storing the project and tracking development over time. |

---

# Application Architecture

Finance Platform will use a straightforward separation between the frontend, backend and database.

## Figure 3.1 – Application Architecture

```text
┌─────────────────────────────┐
│            User             │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│          Frontend           │
│                             │
│     HTML / CSS / JavaScript │
└──────────────┬──────────────┘
               │
          HTTP Requests
               │
               ▼
┌─────────────────────────────┐
│           Backend           │
│                             │
│             PHP             │
└──────────────┬──────────────┘
               │
           SQL Queries
               │
               ▼
┌─────────────────────────────┐
│          Database           │
│                             │
│           MySQL             │
└─────────────────────────────┘
```

### Frontend

The frontend will be responsible for presenting information to the user and allowing them to interact with Finance Platform.

HTML will provide the structure of the pages, CSS will control the appearance and layout, and JavaScript will provide additional client-side functionality.

### Backend

PHP will act as the main server-side component of the application. It will process requests from the frontend, perform calculations and communicate with the MySQL database.

PHP will also be responsible for functionality such as authentication, session management, validation and updating financial records.

### Database

MySQL will store the persistent information required by Finance Platform. PHP will communicate with MySQL using SQL queries to retrieve, insert, update and delete data.

---

# Database Design

A relational MySQL database will be used to store the application's information.

Separate tables will be used for the major financial categories rather than placing all asset types into one generic table.

## Figure 3.2 – Initial Database Structure

```text
MySQL Database
│
├── Users
│
├── Savings
│
├── Investments
│
├── Gold
│
├── Properties
│
├── Loans
│
├── Miscellaneous
│
└── Asset History
```

This structure allows different categories to store information that is specific to them.

For example, Gold may require information about both its weight and monetary value, whereas a savings account primarily requires information about its account and balance.

The exact fields, relationships and database schema will be established during implementation and may be refined as development progresses.

---

# Database Relationships

The database will use relationships between tables where required.

A user's financial information must be associated with the correct user account. Therefore, financial records will be linked to users through appropriate identifiers.

Historical records will also need to be associated with the relevant financial record so that previous values can be retrieved when generating historical information.

## Figure 3.3 – Basic Database Relationship

```text
Users
  │
  ├────────── Savings
  │
  ├────────── Investments
  │
  ├────────── Gold
  │
  ├────────── Properties
  │
  ├────────── Loans
  │
  └────────── Miscellaneous

Financial Records
  │
  └────────── Asset History
```

The database design may be refined during implementation if a different structure proves more suitable.

---

# Data Flow

The basic flow of information through the application will follow the structure below.

## Figure 3.4 – Basic Data Flow

```text
User interacts with webpage
          │
          ▼
HTML / JavaScript sends request
          │
          ▼
PHP receives request
          │
          ▼
PHP validates input
          │
          ▼
PHP processes request
          │
          ▼
MySQL stores or retrieves data
          │
          ▼
PHP processes returned data
          │
          ▼
Frontend displays result
```

This approach keeps database operations on the server side rather than allowing the user to communicate directly with the database.

---

# Graphs and Data Visualisation

Finance Platform will require visual representations of financial information, including:

- Wealth distribution through a pie chart.
- Net worth history through a graph.

These visualisations will be created using JavaScript.

The developer intends to implement the graph and chart functionality themselves rather than relying entirely on a pre-built charting solution. This provides greater control over how financial information is presented and also supports development of JavaScript skills.

The exact implementation of the visualisations will be determined during development.

---

# Authentication and Security

Security is particularly important because Finance Platform will store personal financial information.

The following security measures will be included in the technical implementation.

### Password Hashing

Passwords will not be stored as plain text. Passwords will be securely hashed before being stored in the database.

### Session Management

PHP sessions will be used to keep track of authenticated users. Protected pages will check whether a valid session exists before allowing access.

### Input Validation

User input will be validated before it is processed or stored. This will help prevent invalid information from entering the database and reduce the risk of malicious input.

### Database Security

Database queries will be handled by the PHP backend rather than directly by the frontend.

Further security measures will be considered and implemented as development progresses.

---

# Development Structure

The project will use a simple development structure rather than introducing unnecessary frameworks or complex architecture.

The initial implementation will focus on creating a working Beta using the technologies already selected.

The project will follow the principle:

> **Keep the initial implementation simple, then refactor where necessary.**

This means that the first implementation does not need to be the final structure. As the project becomes larger, repeated code, inefficient structures or areas that could be improved can be identified and refactored.

This approach allows development to progress without attempting to solve every potential future problem before the core system exists.

---

# Version Control

Git and GitHub will be used throughout development.

Git will be used to track changes to the source code, while GitHub will provide the remote repository for the project.

Version control will allow:

- Changes to be recorded.
- Previous versions to be reviewed.
- Development progress to be tracked.
- Mistakes to be reversed where necessary.
- Different stages of development to be maintained.

GitHub will therefore act as both a development tool and a record of the project's development history.

---

# Technical Principles

The following principles will guide implementation.

| Principle | Application |
|-----------|-------------|
| **Simplicity** | The Beta will avoid unnecessary technologies and complexity. |
| **Familiarity** | Technologies already understood by the developer will be prioritised where suitable. |
| **Separation** | Frontend, backend and database responsibilities will remain separated. |
| **Security** | Authentication, password hashing, sessions and validation will be incorporated into the system. |
| **Maintainability** | Code will be kept understandable so that it can be modified and refactored later. |
| **Version Control** | Git and GitHub will be used throughout development. |
| **Refactoring** | The system can be improved and reorganised as development progresses. |

---

# Beta Feature Technical Mapping

The technical design supports the Beta Features established during the analysis phase.

| Beta Feature | Main Technical Components |
|--------------|---------------------------|
| **BF1 – User Authentication** | PHP, MySQL, Sessions, Password Hashing, Validation |
| **BF2 – Dashboard** | PHP, HTML, CSS, JavaScript, MySQL |
| **BF3 – Wealth Distribution** | PHP, MySQL, JavaScript, HTML, CSS |
| **BF4 – Net Worth History** | PHP, MySQL, JavaScript, HTML, CSS |
| **BF5 – Asset Management** | PHP, MySQL, HTML, CSS, JavaScript |
| **BF6 – Savings Management** | PHP, MySQL |
| **BF7 – Investment Management** | PHP, MySQL |
| **BF8 – Property Management** | PHP, MySQL |
| **BF9 – Physical Asset Management** | PHP, MySQL |
| **BF10 – Liability Management** | PHP, MySQL |
| **BF11 – Historical Asset Tracking** | PHP, MySQL |
| **BF12 – Manual Value Updates** | PHP, MySQL, Validation |
| **BF13 – Settings Management** | PHP, MySQL, Sessions, HTML, CSS, JavaScript |

---

## Summary

### Key Points

- Finance Platform will be developed as a web application.
- HTML, CSS and JavaScript will be used for the frontend.
- PHP will be used for server-side functionality.
- MySQL will be used as the relational database.
- Separate database tables will be used for the major financial categories.
- JavaScript will be used to create the project's graphs and charts.
- Authentication will use password hashing, sessions and input validation.
- Git and GitHub will be used for version control and development history.
- The Beta will prioritise simplicity and understandable code.
- Refactoring will be used later where the initial implementation can be improved.
- The technical design directly supports the Beta Features established during the analysis phase.

---

## Related Documents

**Previous**

02_Component_Decomposition.md

**Next**

04_Screen_Designs.md

**Related**

06_Proposed_Solution.md

07_Success_Criteria.md

08_Limitations.md

Testing/Test_Plan.md