# 07 - Test Plan

## Purpose

This document outlines the testing strategy that will be followed throughout the development of the Finance Platform. It defines how the application will be tested during implementation and after development has been completed to ensure it satisfies the functional requirements and success criteria established during the planning phase.

---

# Introduction

Testing is an essential part of the software development process. It ensures that the Finance Platform performs as intended, produces the expected outputs and identifies defects before the application is considered complete.

Throughout development, testing will be carried out iteratively. After implementing each Beta Feature, the corresponding tests will be executed to verify that the feature functions correctly. Should any test fail, the feature will be modified and retested until all expected outcomes have been achieved.

Once development has been completed, the application will undergo a final round of post-development testing to verify that the system functions correctly as a whole and satisfies every planned requirement.

---

# Testing Strategy

Testing will be divided into two stages:

- Iterative Testing
- Post-Development Testing

Iterative testing will be performed continuously throughout development after each Beta Feature has been implemented. This allows defects to be identified and corrected before additional functionality is introduced.

Post-development testing will be performed once the application has been completed. This stage will verify that all features work together correctly and that the application satisfies the original project objectives.

---

# Iterative Testing

Iterative testing will follow the same process throughout development.

```text
Implement Feature
        │
        ▼
 Execute Planned Tests
        │
        ▼
  Do all tests pass?
     │         │
    Yes        No
     │         │
     ▼         ▼
Next Feature  Modify Feature
     ▲         │
     └─────────┘
```

This cycle will continue until every Beta Feature has passed all planned tests.

---

# Iterative Test Cases

## BF1 – User Authentication

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF1 | 1 | Can a new user register? | Users can register an account. | Valid | Confirms new users can create an account. | Account is created and stored within the database. |
| BF1 | 2 | Can an existing user log in? | Users can log in using valid credentials. | Valid | Verifies authentication works correctly. | User is redirected to the dashboard. |
| BF1 | 3 | Invalid password entered. | Invalid login attempts display an error message. | Invalid | Prevents unauthorised access. | Login denied and an error message displayed. |
| BF1 | 4 | Can the user log out? | Users can log out successfully. | Normal | Ensures sessions terminate correctly. | User is returned to the login page. |
| BF1 | 5 | Attempt to access a protected page without logging in. | Protected pages cannot be accessed without authentication. | Invalid | Verifies page protection. | User is redirected to the login page. |

---

## BF2 – Dashboard

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF2 | 6 | Does total net worth display correctly? | Total net worth displayed. | Normal | Confirms calculations are correct. | Net worth equals total assets minus liabilities. |
| BF2 | 7 | Are monetary and percentage changes displayed? | Monetary and percentage changes displayed. | Normal | Ensures financial performance is shown. | Both values appear correctly. |
| BF2 | 8 | Can the user change time periods? | Daily, weekly, monthly, yearly and custom ranges available. | Normal | Verifies dashboard controls. | Dashboard updates to selected period. |
| BF2 | 9 | Does changing an asset update the dashboard? | Dashboard updates automatically. | Normal | Confirms dynamic calculations. | Dashboard reflects latest values. |
| BF2 | 10 | Are navigation shortcuts available? | Dashboard provides quick access to major areas. | Normal | Improves usability. | All navigation links function correctly. |

---

## BF3 – Wealth Distribution

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF3 | 11 | Does the pie chart display every asset category? | All categories shown. | Normal | Ensures complete visualisation. | Every asset category appears. |
| BF3 | 12 | Do chart percentages total 100%? | Percentages total 100%. | Normal | Confirms calculations. | Total equals exactly 100%. |
| BF3 | 13 | Are values taken from the database correctly? | Values accurately represent stored data. | Normal | Verifies database integration. | Chart matches database values. |
| BF3 | 14 | Does updating an asset update the chart? | Chart updates automatically. | Normal | Confirms live updates. | Pie chart refreshes immediately. |

---

## BF4 – Net Worth History

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF4 | 15 | Does the graph display correctly? | Historical graph displayed. | Normal | Confirms graph rendering. | Graph loads successfully. |
| BF4 | 16 | Is data displayed chronologically? | Chronological order maintained. | Normal | Ensures accurate history. | Oldest to newest values shown correctly. |
| BF4 | 17 | Can different date ranges be viewed? | Different time periods available. | Normal | Improves analysis. | Selected range displayed. |
| BF4 | 18 | Does the graph preserve historical values after updates? | Historical records remain unchanged. | Normal | Verifies history integrity. | Previous values remain available. |

---

## BF5 – Asset Management

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF5 | 19 | Can each asset category be accessed? | Every category accessible. | Normal | Confirms navigation. | Selected page loads correctly. |
| BF5 | 20 | Does each category display independent data? | Categories managed independently. | Normal | Prevents data overlap. | Only relevant assets appear. |
| BF5 | 21 | Can users navigate between categories? | Navigation functions correctly. | Normal | Confirms usability. | Navigation works without errors. |

---

## BF6 – Savings Management

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF6 | 22 | Can a new savings account be added? | Users can add savings accounts. | Valid | Verifies account creation. | Savings account is stored successfully within the database. |
| BF6 | 23 | Can an existing savings account be edited? | Users can edit savings accounts. | Normal | Ensures account details remain accurate. | Updated information is saved correctly. |
| BF6 | 24 | Can a savings account be deleted? | Users can delete savings accounts. | Normal | Confirms users can remove unwanted accounts. | Selected savings account is removed. |
| BF6 | 25 | Can the account balance be updated? | Users can manually update balances. | Normal | Verifies balance updates. | New balance is stored correctly. |
| BF6 | 26 | Does updating a balance affect net worth? | Savings contribute correctly to net worth. | Normal | Confirms dashboard calculations. | Net worth updates automatically. |

---

## BF7 – Investment Management

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF7 | 27 | Can a new investment be added? | Users can add investments. | Valid | Verifies investment creation. | Investment is stored successfully. |
| BF7 | 28 | Can an investment be edited? | Users can edit investments. | Normal | Allows users to maintain accurate records. | Investment information is updated correctly. |
| BF7 | 29 | Can an investment be deleted? | Users can delete investments. | Normal | Removes unwanted investments. | Investment is deleted successfully. |
| BF7 | 30 | Can an investment value be updated? | Users can manually update investment values. | Normal | Confirms valuation updates. | Current value is updated correctly. |
| BF7 | 31 | Does updating an investment affect net worth? | Investment values contribute correctly to net worth. | Normal | Verifies financial calculations. | Dashboard reflects updated investment value. |

---

## BF8 – Property Management

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF8 | 32 | Can a new property be added? | Users can add properties. | Valid | Verifies property creation. | Property is successfully stored. |
| BF8 | 33 | Can property information be edited? | Users can edit property information. | Normal | Allows property details to remain current. | Updated property information is saved. |
| BF8 | 34 | Can a property be deleted? | Users can delete properties. | Normal | Removes unwanted properties. | Property is deleted successfully. |
| BF8 | 35 | Can a property's valuation be updated? | Users can manually update property valuations. | Normal | Confirms property value updates. | Updated valuation is stored correctly. |
| BF8 | 36 | Does updating a property affect net worth? | Property values contribute correctly to net worth. | Normal | Verifies dashboard calculations. | Net worth recalculates automatically. |

---

## BF9 – Miscellaneous Asset Management

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF9 | 37 | Can a miscellaneous asset be added? | Users can add miscellaneous assets. | Valid | Verifies creation of miscellaneous assets. | Asset is successfully added to the database. |
| BF9 | 38 | Can a miscellaneous asset be edited? | Users can edit miscellaneous assets. | Normal | Allows users to maintain accurate information. | Changes are saved correctly. |
| BF9 | 39 | Can a miscellaneous asset be deleted? | Users can delete miscellaneous assets. | Normal | Removes unwanted records. | Asset is removed successfully. |
| BF9 | 40 | Can the estimated value be updated? | Users can manually update asset values. | Normal | Verifies valuation updates. | Estimated value is updated successfully. |
| BF9 | 41 | Does updating the value affect net worth? | Miscellaneous assets contribute correctly to net worth. | Normal | Confirms calculations remain accurate. | Dashboard updates automatically. |

---

## BF10 – Liability Management

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF10 | 42 | Can a new liability be added? | Users can add liabilities. | Valid | Verifies liability creation. | Liability is successfully stored. |
| BF10 | 43 | Can a liability be edited? | Users can edit liabilities. | Normal | Keeps liability information accurate. | Updated information is saved correctly. |
| BF10 | 44 | Can a liability be deleted? | Users can delete liabilities. | Normal | Removes unnecessary liabilities. | Liability is deleted successfully. |
| BF10 | 45 | Can the remaining balance be updated? | Users can manually update liability values. | Normal | Confirms outstanding balances can be maintained. | Updated balance is stored successfully. |
| BF10 | 46 | Does updating a liability reduce net worth correctly? | Liabilities reduce total net worth correctly. | Normal | Verifies financial calculations. | Net worth decreases appropriately after the update. |

---

## BF11 – Historical Asset Tracking

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF11 | 47 | Does updating an asset create a historical record? | Every value update creates a historical record. | Normal | Ensures historical information is preserved. | Previous asset data is copied into the corresponding history table. |
| BF11 | 48 | Can historical records be modified? | Historical records cannot be modified retrospectively. | Invalid | Prevents accidental alteration of historical data. | User cannot edit existing history records. |
| BF11 | 49 | Are the correct value and timestamp stored? | Correct value and timestamp stored for every update. | Normal | Verifies data integrity. | History record contains the previous value together with the correct date and time. |
| BF11 | 50 | Can historical records be viewed? | Historical data available for charts and asset history pages. | Normal | Ensures historical information can be analysed. | Previous values are displayed correctly within graphs and history pages. |

---

## BF12 – Manual Value Updates

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF12 | 51 | Can every supported asset be manually updated? | Users can manually update every supported asset type. | Normal | Verifies update functionality across all asset categories. | Selected asset is updated successfully. |
| BF12 | 52 | Does updating an asset immediately recalculate net worth? | Net worth recalculates immediately. | Normal | Ensures dashboard remains accurate. | Updated total net worth is displayed instantly. |
| BF12 | 53 | Is a historical record automatically created? | Historical values stored automatically. | Normal | Confirms historical tracking. | Previous value is copied into the relevant history table. |
| BF12 | 54 | Are updated values reflected throughout the application? | Updated values reflected throughout the application. | Normal | Ensures application consistency. | Dashboard, graphs and asset pages all display the updated value. |

---

## BF13 – Settings Management

| Feature | Test No. | Test | Success Criteria | Input Type | Justification | Expected Result |
|----------|----------|------|------------------|------------|---------------|-----------------|
| BF13 | 55 | Can the user update their profile information? | Users can update profile information. | Normal | Allows personal information to remain accurate. | Updated information is saved successfully. |
| BF13 | 56 | Can the user change their password? | Users can change account password. | Valid | Improves account security. | New password replaces the existing password. |
| BF13 | 57 | Can application preferences be modified? | Users can modify application preferences. | Normal | Allows limited personalisation of the application. | Preference changes are saved correctly. |
| BF13 | 58 | Are settings retained after logging out? | Settings persist between sessions. | Normal | Confirms settings are permanently stored. | Updated settings remain after logging back in. |

---

# Post-Development Testing

Once implementation has been completed, the Finance Platform will undergo a comprehensive round of testing to ensure the application functions correctly as a complete system.

Unlike iterative testing, which focuses on individual Beta Features during development, post-development testing evaluates the application as a whole. This stage confirms that all implemented features work together correctly and that changes made during development have not introduced unexpected behaviour elsewhere within the system.

The following forms of testing will be performed.

| Testing Type | Purpose |
|--------------|---------|
| Functional Testing | Confirms every feature performs as intended. |
| User Interface Testing | Ensures layouts, navigation and controls remain consistent and intuitive. |
| Database Testing | Verifies records are stored, updated and retrieved correctly. |
| Compatibility Testing | Ensures the application functions correctly across supported web browsers. |
| Performance Testing | Confirms the application remains responsive when storing and displaying larger quantities of financial data. |
| User Acceptance Testing | Allows stakeholders to evaluate the completed application and provide feedback on usability and functionality. |

During post-development testing, evidence will be collected for every completed test.

Evidence may include:

- Screenshots
- Database records
- Expected results
- Actual results
- Pass / Fail outcome
- Bug fixes where applicable

---

# Summary

The Finance Platform will be tested using an iterative development strategy supported by a comprehensive post-development testing phase.

Throughout implementation, every Beta Feature will be tested immediately after development. If any planned test fails, the feature will be corrected and retested before development continues. This iterative approach allows defects to be identified early while ensuring completed features remain stable throughout the remainder of the project.

Following implementation, a final round of testing will evaluate the application as a complete system, verifying that all planned functionality has been implemented successfully and that the Finance Platform satisfies both its success criteria and overall project objectives.

---

## Related Documents

**Previous**

06_Development_Methodology.md

**Next**


**Related**

07_Success_Criteria.md

06_Proposed_Solution.md