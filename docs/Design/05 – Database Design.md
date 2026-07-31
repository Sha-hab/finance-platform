# 05 – Database Design

## Purpose

This document explains the design of the Finance Platform database and the principles used to organise and store application data. It outlines how data will be structured, how relationships between tables are maintained, and how the design supports the Beta Features identified within the proposed solution.

---

# Introduction

The Finance Platform requires a database capable of storing financial information securely while remaining efficient, scalable and easy to maintain. A relational database model has been selected as it provides a structured method of organising data through related tables, reducing unnecessary duplication and improving data integrity.

The database has been designed to closely reflect the application's functionality. Each major asset category has its own dedicated table, making the database easier to understand, develop and maintain while providing a direct relationship between the application's user interface and its underlying data.

---

# Database Design

The database has been divided into multiple related tables rather than storing all information within a single table.

Each table is responsible for storing information about a single entity, including:

- Users
- Savings
- Investments
- Properties
- Loans
- Miscellaneous Assets
- Historical records for each asset category

Separating data into individual tables improves organisation, simplifies queries and allows additional records to be added without affecting existing data.

Each financial category is linked directly to its owning user, allowing every user to manage multiple assets across different categories while ensuring all information remains associated with the correct account.

Historical records are stored separately from the current asset values. Whenever an asset is updated, the existing record is copied into its corresponding history table before the live record is modified. This allows previous values to be viewed while ensuring the main asset tables always contain the most recent information.

---

# Primary Keys

Every table contains a **Primary Key**.

A primary key is a unique identifier that distinguishes each record from every other record stored within the table.

For example:

- UserID
- SavingsID
- InvestmentID
- PropertyID
- LoanID
- MiscID

Each primary key uses an automatically incrementing integer value. This guarantees that every record has a unique identifier and allows records to be referenced efficiently by other tables.

---

# Foreign Keys

Relationships between tables are created using **Foreign Keys**.

A foreign key stores the primary key of another table, allowing related records to be linked together.

For example, every financial asset stores the **UserID** of its owner. This creates a one-to-many relationship where a single user can own multiple savings accounts, investments, properties, loans and miscellaneous assets.

Using foreign keys maintains referential integrity by ensuring that every financial record always belongs to a valid user.

---

# Relationships

The database follows a relational structure where one user may own multiple financial assets across different categories.

The primary relationships are:

- One User can own many Savings Accounts.
- One User can own many Investments.
- One User can own many Properties.
- One User can own many Loans.
- One User can own many Miscellaneous Assets.

Each financial category also maintains its own history table.

Whenever an asset is modified, the previous version of that asset is stored within its corresponding history table before the live record is updated. This allows historical information to be preserved without affecting the current asset values displayed throughout the application.

These relationships will be illustrated fully within the Entity Relationship Diagram presented in the following document.

---

# Normalisation

The database has been designed using the principles of **database normalisation**.

Normalisation is the process of organising data into separate tables to reduce unnecessary duplication while improving consistency and maintainability.

Rather than storing all financial information within a single table, the application separates each major asset category into its own dedicated table. User information is also stored independently from financial data and linked through foreign keys.

This approach provides several advantages:

- Reduces duplicate data.
- Improves database consistency.
- Simplifies future maintenance.
- Reduces storage requirements.
- Allows the database to expand without significant redesign.

The resulting database closely follows the principles of Third Normal Form (3NF), where each table stores information relating to a single entity and relationships are used to connect related data.

---

# Redundancy

One of the primary objectives of the database design was to minimise **data redundancy**.

Data redundancy occurs when the same information is stored repeatedly across multiple records or tables.

Within the Finance Platform, user information is stored only once inside the Users table. Financial assets do not store duplicate user details such as names or email addresses. Instead, each asset stores only the UserID required to identify its owner.

Similarly, historical records are stored separately from current asset values. This prevents multiple versions of the same asset being stored within the primary asset tables while still preserving previous versions for historical analysis.

Reducing redundancy improves data accuracy, simplifies updates and decreases the likelihood of inconsistent information being stored.

---

# Database Structure

The Finance Platform database has been designed around the application's major financial categories. Rather than storing every asset within a single table, each category is maintained independently. This mirrors the application's navigation structure, simplifies queries and allows each asset type to store information relevant to that category.

At the centre of the database is the **Users** table. Every account created within the application is stored here and each user is assigned a unique UserID. This identifier is then referenced by all financial asset tables using foreign keys, allowing every asset to be associated with its owner.

The database consists of the following primary tables:

- Users
- Savings
- Investments
- Properties
- Loans
- Miscellaneous

Each of these tables also has a corresponding history table:

- SavingsHistory
- InvestmentsHistory
- PropertiesHistory
- LoansHistory
- MiscellaneousHistory

This results in a total of **eleven tables** within the database.

The overall database structure is illustrated below.

```text
Users
│
├── Savings
│   └── SavingsHistory
│
├── Investments
│   └── InvestmentsHistory
│
├── Properties
│   └── PropertiesHistory
│
├── Loans
│   └── LoansHistory
│
└── Miscellaneous
    └── MiscellaneousHistory
```

The **Users** table stores account information required for authentication, including the user's name, email address and encrypted password. No financial information is stored within this table. Instead, every financial asset references the owning user through the UserID foreign key.

The **Savings** table stores information relating to savings accounts, including the bank, account name, current balance, notes and the date the account was last updated. Users may store multiple savings accounts, including multiple accounts with the same bank.

The **Investments** table stores all investment assets. This includes traditional investments such as shares and exchange-traded funds, alongside physical investments such as precious metals. Each record stores the asset name, quantity owned, current valuation, notes and the date the value was last updated.

The **Properties** table stores information relating to real estate owned by the user. Each property records its current market value, full address and optional rental income. Rental income is stored for reference purposes only and does not contribute towards the property's valuation. Mortgages are intentionally stored separately within the Loans table, ensuring that assets and liabilities remain independent.

The **Loans** table stores all financial liabilities, including mortgages, student loans, personal loans and vehicle finance. Each record stores the remaining balance owed together with the lender and any supporting notes.

The **Miscellaneous** table stores financial assets that do not naturally belong within any of the other categories. This allows the application to remain flexible while avoiding unnecessary database redesign whenever users wish to record uncommon asset types.

Each financial table is paired with a corresponding history table. Whenever a user updates an asset, the existing record is copied into its history table before the current record is modified. This preserves a complete historical snapshot of the asset while ensuring that the primary asset tables always contain the most recent information.

Separating current records from historical records provides two important benefits. Firstly, it keeps the primary tables small and efficient for everyday queries. Secondly, it allows historical values to be viewed, analysed and displayed within graphs without affecting the live data shown throughout the application.

---

# Summary

The Finance Platform database has been designed using a relational structure that promotes simplicity, scalability and maintainability.

The use of primary keys uniquely identifies every record, while foreign keys establish relationships between users and their financial assets. Data has been organised using normalisation principles to minimise redundancy and improve consistency throughout the application.

By separating each financial category into its own table and maintaining dedicated history tables, the database provides an efficient foundation for both the current Beta Features and future expansion of the Finance Platform.

---

## Related Documents

**Previous**

04_Screen_Designs.md

**Next**

06_Entity_Relationship_Diagram.md

**Related**

06_Proposed_Solution.md

07_Success_Criteria.md