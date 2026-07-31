# 01 - System Decomposition

## Purpose

This document decomposes Finance Platform into progressively smaller components. Beginning with the overall system, each major subsystem is broken down into smaller functional components until each represents a feature that can later be designed, implemented and tested.

---

# Introduction

Before implementation begins, it is important to understand how Finance Platform is organised internally. Decomposition breaks the system into smaller components so that each part can be designed and developed independently while maintaining a clear relationship with the overall system.

This document establishes the overall structure of the application and provides the foundation for the remaining design documentation. The components identified here will be broken down further into individual features in later design documents.

---

# System Decomposition

## Figure 1.1 – Overall System

```text
Finance Platform
│
├── Authentication
├── Dashboard
├── Asset Management
└── Settings
```

The overall system is divided into four main components. Authentication controls access to the application, the Dashboard provides the user's financial overview, Asset Management contains the user's financial information, and Settings manages account and application preferences.

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF1** | Authentication | Responsible for user registration, authentication and session management. |
| **BF2–BF5** | Dashboard | Displays an overview of the user's financial position and provides access to the main areas of the application. |
| **BF5–BF12** | Asset Management | Allows users to manage assets and liabilities that contribute to their overall net worth. |
| **BF13** | Settings | Allows users to manage account information, security and application preferences. |

---

# Authentication Decomposition

## Figure 1.2 – Authentication

```text
Authentication
│
├── Registration
├── Login
├── Password Recovery
└── Logout
```

Authentication is responsible for allowing users to create and access their accounts. These components work together to ensure that users can securely access their own financial information.

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF1** | Registration | Allows a new user to create an account. |
| **BF1** | Login | Allows an existing user to access their account using valid credentials. |
| **BF1** | Password Recovery | Allows a user to recover access to their account if they forget their password. |
| **BF1** | Logout | Ends the user's active session and prevents further access to protected pages. |

---

# Dashboard Decomposition

## Figure 1.3 – Dashboard

```text
Dashboard
│
├── Net Worth Summary
├── Wealth Distribution
├── Net Worth History
├── Recent Changes
└── Asset Navigation
```

The Dashboard is the main screen of Finance Platform. It is designed to allow users to understand their overall financial position without having to inspect every individual asset.

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF2** | Net Worth Summary | Displays the user's current total net worth together with monetary and percentage changes. |
| **BF3** | Wealth Distribution | Displays how the user's wealth is distributed across the different asset categories. |
| **BF4** | Net Worth History | Displays how the user's overall net worth has changed over time. |
| **BF2–BF4** | Recent Changes | Displays recent changes to the user's financial information. |
| **BF5** | Asset Navigation | Provides access to the different asset management sections. |

---

# Asset Management Decomposition

## Figure 1.4 – Asset Management

```text
Asset Management
│
├── Savings
├── Investments
├── Property
├── Loans
└── Miscellaneous
```

Asset Management is responsible for storing and managing the different forms of wealth and liabilities supported by Finance Platform. Each category is separated so that different types of financial information can be managed independently.

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF6** | Savings | Manages the user's savings accounts and their balances. |
| **BF7** | Investments | Manages long-term investments such as stocks, ETFs, funds, bonds and cryptocurrency. |
| **BF9** | Precious materials | Manages material holdings and their current values. |
| **BF8** | Property | Manages property owned by the user and its current value. |
| **BF10** | Loans | Manages mortgages and other liabilities owed by the user. |
| **BF9** | Miscellaneous | Manages other valuable assets that do not belong to the other categories. |

---

# Settings Decomposition

## Figure 1.5 – Settings

```text
Settings
│
├── Profile
├── Security
├── Preferences
└── About
```

Settings provides a separate area for account and application configuration. Keeping these functions separate from the financial management system prevents account configuration from being mixed with the user's financial information.

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF13** | Profile | Allows users to view and update their account information. |
| **BF13** | Security | Allows users to manage their password and account security. |
| **BF13** | Preferences | Allows users to modify available application preferences. |
| **BF13** | About | Provides information about Finance Platform and the current Beta release. |

---

# Beta Feature Traceability

The decomposition has been cross-referenced with the Beta Features to ensure that every proposed feature has a corresponding component within the system.

| Beta Feature | Decomposed Component |
|--------------|----------------------|
| **BF1 – User Authentication** | Authentication |
| **BF2 – Dashboard** | Dashboard → Net Worth Summary |
| **BF3 – Wealth Distribution** | Dashboard → Wealth Distribution |
| **BF4 – Net Worth History** | Dashboard → Net Worth History |
| **BF5 – Asset Management** | Dashboard → Asset Navigation / Asset Management |
| **BF6 – Savings Management** | Asset Management → Savings |
| **BF7 – Investment Management** | Asset Management → Investments |
| **BF8 – Property Management** | Asset Management → Property |
| **BF9 – Physical Asset Management** | Asset Management → Gold / Miscellaneous |
| **BF10 – Liability Management** | Asset Management → Loans |
| **BF11 – Historical Asset Tracking** | Dashboard → Net Worth History / Asset Management |
| **BF12 – Manual Value Updates** | Asset Management → Individual Asset Categories |
| **BF13 – Settings Management** | Settings |

---

## Summary

### Key Points

- Finance Platform has been divided into four primary system components.
- Each primary component has been decomposed into smaller functional components.
- The decomposition provides a clear structure for the next stages of the design process.
- Every Beta Feature has been cross-referenced with a component of the system.
- Individual components will be decomposed further into their specific features in later design documents.
- Testing and test cases are intentionally not included at this stage and will be addressed during the testing phase.

---

## Related Documents

**Previous**

08_Limitations.md

**Next**

02_Component_Decomposition.md

**Related**

06_Proposed_Solution.md

07_Success_Criteria.md

Testing/Test_Plan.md