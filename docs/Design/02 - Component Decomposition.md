# 02 - Component Decomposition

## Purpose

This document breaks down the main components identified in the System Decomposition into their individual functional components. The purpose is to establish what each major section of Finance Platform is made up of before individual features are designed.

---

# Introduction

The System Decomposition established four main areas of Finance Platform:

- Authentication
- Dashboard
- Asset Management
- Settings

This document takes each of these areas and decomposes them further. The components identified here will form the basis for the next stage of design, where individual components will be broken down into more specific features and requirements.

The decomposition is cross-referenced with the Beta Features established during the analysis phase to maintain traceability between the proposed solution and the design.

---

# Authentication Decomposition

Authentication is responsible for allowing users to create and access their accounts securely.

## Figure 2.1 – Authentication Decomposition

```text
Authentication
│
├── Registration
├── Login
├── Password Recovery
└── Logout
```

### Table 2.1 – Authentication Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF1** | Registration | Allows new users to create an account. |
| **BF1** | Login | Allows existing users to access their account using their credentials. |
| **BF1** | Password Recovery | Allows users to recover access to their account if they forget their password. |
| **BF1** | Logout | Allows users to securely end their current session. |

---

# Dashboard Decomposition

The Dashboard is the main overview of Finance Platform. It presents the user's overall financial position and provides access to the different areas of the application.

## Figure 2.2 – Dashboard Decomposition

```text
Dashboard
│
├── Net Worth Summary
│   ├── Current Net Worth
│   ├── Monetary Change
│   ├── Percentage Change
│   └── Time Period Selection
│       ├── Daily
│       ├── Weekly
│       ├── Monthly
│       ├── Yearly
│       └── Custom
│
├── Wealth Distribution
│   ├── Asset Category Values
│   ├── Percentage Calculations
│   └── Pie Chart
│
├── Net Worth History
│   ├── Historical Data
│   ├── Time Period Selection
│   └── Net Worth Graph
│
└── Asset Navigation
    ├── Savings
    ├── Investments
    ├── Gold
    ├── Property
    ├── Loans
    └── Miscellaneous
```

### Table 2.2 – Dashboard Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF2** | Current Net Worth | Displays the user's current total net worth prominently on the Dashboard. |
| **BF2** | Monetary Change | Displays the monetary change in net worth for the selected period. |
| **BF2** | Percentage Change | Displays the percentage change in net worth for the selected period. |
| **BF2** | Time Period Selection | Allows the user to change the period used to calculate the displayed change. |
| **BF3** | Asset Category Values | Provides the values required to determine the distribution of the user's wealth. |
| **BF3** | Percentage Calculations | Calculates the proportion of total wealth represented by each asset category. |
| **BF3** | Pie Chart | Visually displays the distribution of wealth between asset categories. |
| **BF4, BF11** | Historical Data | Provides previously recorded net worth values for historical analysis. |
| **BF4** | Time Period Selection | Allows the user to select the period displayed by the net worth graph. |
| **BF4** | Net Worth Graph | Displays changes in the user's net worth over time. |
| **BF5** | Asset Navigation | Provides access to the different asset management categories. |

---

# Asset Management Decomposition

Asset Management contains the different categories used to organise the user's wealth and liabilities.

Each category is kept separate because the information required to manage one type of asset may differ from another.

## Figure 2.3 – Asset Management Decomposition

```text
Asset Management
│
├── Savings
│   ├── Add Savings Account
│   ├── View Savings Account
│   ├── Edit Savings Account
│   ├── Delete Savings Account
│   └── Update Balance
│
├── Investments
│   ├── Add Investment
│   ├── View Investment
│   ├── Edit Investment
│   ├── Delete Investment
│   └── Update Investment Value
│
├── Gold
│   ├── Add Gold Holding
│   ├── View Gold Holding
│   ├── Edit Gold Holding
│   ├── Delete Gold Holding
│   └── Update Gold Weight and Value
│
├── Property
│   ├── Add Property
│   ├── View Property
│   ├── Edit Property
│   ├── Delete Property
│   └── Update Property Value
│
├── Loans
│   ├── Add Loan
│   ├── View Loan
│   ├── Edit Loan
│   ├── Delete Loan
│   └── Update Loan Balance
│
└── Miscellaneous
    ├── Add Asset
    ├── View Asset
    ├── Edit Asset
    ├── Delete Asset
    └── Update Asset Value
```

---

## Savings

Savings Management allows users to record and maintain their savings accounts.

### Table 2.3 – Savings Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF6** | Add Savings Account | Allows users to add a savings account to Finance Platform. |
| **BF6** | View Savings Account | Allows users to view information about their savings accounts. |
| **BF6** | Edit Savings Account | Allows users to change information associated with a savings account. |
| **BF6** | Delete Savings Account | Allows users to remove a savings account from the system. |
| **BF6, BF12** | Update Balance | Allows users to manually update the balance of a savings account. |

---

## Investments

Investment Management allows users to record and maintain their long-term investments.

The specific investment types supported by the Beta will be established during the later feature design rather than being defined further at this stage.

### Table 2.4 – Investment Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF7** | Add Investment | Allows users to add an investment. |
| **BF7** | View Investment | Allows users to view information about their investments. |
| **BF7** | Edit Investment | Allows users to change information associated with an investment. |
| **BF7** | Delete Investment | Allows users to remove an investment from the system. |
| **BF7, BF12** | Update Investment Value | Allows users to manually update the current value of an investment. |

---

## Gold

Gold is treated separately from Miscellaneous because it has specific information that needs to be recorded, particularly its weight and monetary value.

### Table 2.5 – Gold Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF9** | Add Gold Holding | Allows users to add a gold holding. |
| **BF9** | View Gold Holding | Allows users to view information about their gold holdings. |
| **BF9** | Edit Gold Holding | Allows users to change information associated with a gold holding. |
| **BF9** | Delete Gold Holding | Allows users to remove a gold holding from the system. |
| **BF9, BF12** | Update Gold Weight and Value | Allows users to manually update the weight and monetary value of their gold. |

---

## Property

Property Management allows users to record and maintain properties that form part of their overall wealth.

### Table 2.6 – Property Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF8** | Add Property | Allows users to add a property. |
| **BF8** | View Property | Allows users to view information about their properties. |
| **BF8** | Edit Property | Allows users to change information associated with a property. |
| **BF8** | Delete Property | Allows users to remove a property from the system. |
| **BF8, BF12** | Update Property Value | Allows users to manually update the estimated value of a property. |

---

## Loans

Loan Management allows users to record liabilities that affect their overall net worth.

### Table 2.7 – Loan Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF10** | Add Loan | Allows users to add a loan or other liability. |
| **BF10** | View Loan | Allows users to view information about their loans. |
| **BF10** | Edit Loan | Allows users to change information associated with a loan. |
| **BF10** | Delete Loan | Allows users to remove a loan from the system. |
| **BF10, BF12** | Update Loan Balance | Allows users to manually update the outstanding balance of a loan. |

---

## Miscellaneous

Miscellaneous is intended for assets that do not fit naturally into the other predefined categories. Unlike Gold, this category does not have a specific asset type or structure.

### Table 2.8 – Miscellaneous Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF9** | Add Asset | Allows users to add an asset that does not belong to another category. |
| **BF9** | View Asset | Allows users to view information about miscellaneous assets. |
| **BF9** | Edit Asset | Allows users to change information associated with a miscellaneous asset. |
| **BF9** | Delete Asset | Allows users to remove a miscellaneous asset from the system. |
| **BF9, BF12** | Update Asset Value | Allows users to manually update the value of a miscellaneous asset. |

---

# Historical Asset Tracking Decomposition

Historical Asset Tracking is not intended to be a separate area that users navigate to. Instead, it is a system function that operates alongside asset management and stores previous values when assets are updated.

## Figure 2.4 – Historical Asset Tracking Decomposition

```text
Historical Asset Tracking
│
├── Record Value
├── Record Date and Time
└── Retrieve Historical Values
```

### Table 2.9 – Historical Asset Tracking Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF11** | Record Value | Stores the value of an asset at the time an update is made. |
| **BF11** | Record Date and Time | Stores when the historical value was recorded. |
| **BF11** | Retrieve Historical Values | Allows previously recorded values to be retrieved for historical views and graphs. |

Historical Asset Tracking supports both **BF4 – Net Worth History** and the historical information required by individual asset categories.

---

# Manual Value Updates

Manual Value Updates are not treated as a separate user-facing section. Instead, the functionality exists within each asset management category.

## Figure 2.5 – Manual Value Updates

```text
Asset Management
│
├── Savings
│   └── Update Balance
│
├── Investments
│   └── Update Investment Value
│
├── Gold
│   └── Update Gold Weight and Value
│
├── Property
│   └── Update Property Value
│
├── Loans
│   └── Update Loan Balance
│
└── Miscellaneous
    └── Update Asset Value
```

This structure prevents duplicated functionality and ensures that each asset type can update its own value while remaining connected to the overall net worth calculation.

---

# Settings Decomposition

Settings provides users with a separate area for managing their account and application preferences.

## Figure 2.6 – Settings Decomposition

```text
Settings
│
├── Profile
│   ├── View Profile Information
│   └── Update Profile Information
│
├── Security
│   └── Change Password
│
├── Preferences
│   ├── Currency
│   ├── Default Time Period
│   └── Application Preferences
│
└── About
    ├── Application Information
    └── Version Information
```

### Table 2.10 – Settings Components

| Related BF | Component | Description |
|------------|-----------|-------------|
| **BF13** | Profile | Allows users to view and update their account information. |
| **BF13** | Security | Allows users to manage account security, including changing their password. |
| **BF13** | Preferences | Allows users to change available application preferences. |
| **BF13** | About | Provides information about Finance Platform and its current Beta version. |

---

# Component Traceability

The decomposition has been cross-referenced against the Beta Features to ensure that the components identified in this document correspond with the proposed solution.

| Beta Feature | Component(s) |
|--------------|--------------|
| **BF1 – User Authentication** | Authentication |
| **BF2 – Dashboard** | Net Worth Summary |
| **BF3 – Wealth Distribution** | Asset Category Values, Percentage Calculations, Pie Chart |
| **BF4 – Net Worth History** | Historical Data, Time Period Selection, Net Worth Graph |
| **BF5 – Asset Management** | Asset Navigation, Savings, Investments, Gold, Property, Loans, Miscellaneous |
| **BF6 – Savings Management** | Savings |
| **BF7 – Investment Management** | Investments |
| **BF8 – Property Management** | Property |
| **BF9 – Physical Asset Management** | Gold, Miscellaneous |
| **BF10 – Liability Management** | Loans |
| **BF11 – Historical Asset Tracking** | Record Value, Record Date and Time, Retrieve Historical Values |
| **BF12 – Manual Value Updates** | Update Balance, Update Investment Value, Update Gold Weight and Value, Update Property Value, Update Loan Balance, Update Asset Value |
| **BF13 – Settings Management** | Profile, Security, Preferences, About |

---

## Summary

### Key Points

- Each major component identified in the System Decomposition has been broken down into smaller components.
- Dashboard components have been separated according to the information and functionality presented to the user.
- Asset Management has been divided into the six categories established in the proposed solution.
- Gold and Miscellaneous are treated as separate categories because they have different purposes and data requirements.
- Historical Asset Tracking and Manual Value Updates are treated as supporting functions rather than separate navigation areas.
- Every component has been cross-referenced with the relevant Beta Feature.
- The components identified here will be broken down further into individual features during the next stage of the design process.
- Test cases have not been included at this stage and will be developed later during the testing phase.

---

## Related Documents

**Previous**

01_System_Decomposition.md

**Next**

03 - Technical Design.md

**Related**

06_Proposed_Solution.md

07_Success_Criteria.md

08_Limitations.md

Testing/Test_Plan.md