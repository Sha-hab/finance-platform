# 06 - Proposed Solution

## Purpose

This document defines the functionality that will be implemented within the Beta release of Finance Platform. The proposed solution has been developed using the findings gathered throughout the analysis phase, including stakeholder requirements, product research and the overall project vision.

The Beta release focuses on solving the core problem identified during the analysis stage: allowing users to understand where their wealth is held before introducing advanced investment tools or automation.

---

# Introduction

Finance Platform has been designed to provide users with a centralised view of their long-term wealth. Existing financial applications often specialise in a single area, such as investing or budgeting, requiring users to switch between multiple services to understand their complete financial position.

The Beta release addresses this problem by allowing users to manually record, organise and monitor their wealth through a single application. The emphasis is placed on simplicity, clarity and understanding rather than financial optimisation.

The following features define the scope of the Beta release.

---

# Beta Features

| ID | Feature | Description | Justification | Source |
|----|---------|-------------|---------------|--------|
| **BF1** | User Authentication | Allows users to securely register, log in and access their own financial information. | Financial information is private and must only be accessible by the account owner. | Stakeholder Research |
| **BF2** | Dashboard | Displays total net worth as the primary focus together with the overall monetary and percentage change. Users can switch between daily, weekly, monthly and yearly changes. | Users should immediately understand their current financial position when opening the application. | Trading 212 Research |
| **BF3** | Wealth Distribution | Displays a pie chart showing how overall wealth is distributed across each asset category. | Enables users to quickly understand where the majority of their wealth is held. | Product Research |
| **BF4** | Net Worth History | Displays a historical line graph showing how total net worth has changed over time. | Allows users to identify financial trends and monitor long-term growth. | Product Research |
| **BF5** | Asset Categories | Provides dedicated sections for Savings, Investments, Properties, Physical Assets, Liabilities and Miscellaneous assets. | Organises financial information into logical categories while keeping the dashboard simple. | Stakeholder Research |
| **BF6** | Savings Management | Allows users to add, edit and remove savings accounts while manually updating balances. | Enables users to monitor long-term savings held across multiple financial institutions. | Problem Analysis |
| **BF7** | Investment Management | Allows users to record and manage long-term investments including stocks, ETFs, funds, bonds and cryptocurrency. | Investments often represent a significant proportion of long-term wealth and should contribute towards overall net worth. | Stakeholder Research |
| **BF8** | Property Management | Allows users to record property information and manually update property valuations. | Property is commonly one of the largest long-term assets owned by an individual. | Stakeholder Research |
| **BF9** | Physical Asset Management | Allows users to manage valuable physical assets such as gold, silver and other long-term possessions. | Wealth extends beyond bank accounts and investments, therefore physical assets should also be represented. | Stakeholder Research |
| **BF10** | Liability Management | Allows users to record mortgages and other long-term liabilities. | Net worth must accurately consider both assets and liabilities. | Problem Analysis |
| **BF11** | Historical Asset Tracking | Every time an asset value is updated, the previous value is automatically retained as historical data. | Enables graphs, performance tracking and long-term analysis for every asset. | Project Vision |
| **BF12** | Manual Value Updates | Users manually enter updated values whenever they wish to review their finances. | Manual entry keeps the Beta release simple while avoiding external integrations and unnecessary complexity. | Project Scope |
| **BF13** | Responsive Interface | The application will function correctly on desktop, tablet and mobile web browsers. | Users should be able to review their financial information regardless of the device being used. | Stakeholder Research |

---

# Feature Summary

The Beta release has been designed around a single objective:

> **Allow users to understand their overall wealth before attempting to optimise or grow it.**

Every feature included within the Beta release directly contributes towards this objective.

The dashboard provides an immediate overview of total net worth, while supporting graphs and wealth distribution visualisations help users understand how their financial position changes over time. Dedicated asset management pages allow different forms of wealth to be organised into logical categories, ensuring the interface remains simple and intuitive regardless of the user's financial experience.

Features such as live market prices, investment recommendations and automated financial analysis have intentionally been excluded from the Beta release. These enhancements can be considered in future versions once the core wealth tracking functionality has been fully implemented and validated.

---

## Summary

### Key Points

- The Beta release focuses on understanding wealth rather than growing it.
- Users can manage all long-term assets from a single platform.
- Net worth is presented as the primary piece of information throughout the application.
- Historical tracking allows users to monitor financial progress over time.
- Manual data entry has been selected to reduce complexity while establishing a strong foundation for future development.

---

## Related Documents

**Previous**

05_Product_Research.md

**Next**

07_Success_Criteria.md

**Related**

01_Problem_Analysis.md

02_Project_Vision.md

04_Stakeholders.md