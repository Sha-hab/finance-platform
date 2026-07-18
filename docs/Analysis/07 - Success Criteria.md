# 07 - Success Criteria

## Purpose

This document defines the measurable success criteria for each Beta Feature proposed within Finance Platform. These criteria provide a checklist that will be used throughout development and testing to verify that each feature has been implemented successfully.

---

# Introduction

The proposed solution defines what the Beta release should include, however it does not define how success will be measured.

This document establishes measurable success criteria for every Beta Feature. During development and testing, these criteria will be used to verify that each feature performs as intended and satisfies the objectives established during the analysis phase.

---

# Beta Feature Success Criteria

| Feature | Evidence | Success Criteria |
|----------|----------|------------------|
| **BF1 – User Authentication** | Screenshots, Functional Testing | ✓ Users can register an account.<br>✓ Users can log in using valid credentials.<br>✓ Invalid login attempts display an appropriate error message.<br>✓ Users can log out successfully.<br>✓ Protected pages cannot be accessed without authentication. |
| **BF2 – Dashboard** | Screenshots, Functional Testing | ✓ Total net worth is displayed prominently.<br>✓ Monetary change is displayed.<br>✓ Percentage change is displayed.<br>✓ Users can switch between daily, weekly, monthly and yearly views.<br>✓ Dashboard values update after asset values change. |
| **BF3 – Wealth Distribution** | Screenshots, Functional Testing | ✓ Pie chart displays all asset categories.<br>✓ Percentages total 100%.<br>✓ Values accurately represent stored data.<br>✓ Chart updates after asset values change. |
| **BF4 – Net Worth History** | Screenshots, Functional Testing | ✓ Historical graph displays correctly.<br>✓ Data is displayed chronologically.<br>✓ New entries appear after updates.<br>✓ Historical data remains unchanged after further updates. |
| **BF5 – Asset Categories** | Screenshots | ✓ Savings category exists.<br>✓ Investments category exists.<br>✓ Properties category exists.<br>✓ Physical Assets category exists.<br>✓ Liabilities category exists.<br>✓ Miscellaneous category exists.<br>✓ Every category is accessible from the dashboard. |
| **BF6 – Savings Management** | Functional Testing | ✓ Users can add savings accounts.<br>✓ Users can edit savings accounts.<br>✓ Users can delete savings accounts.<br>✓ Users can update balances.<br>✓ Net worth updates correctly. |
| **BF7 – Investment Management** | Functional Testing | ✓ Users can add investments.<br>✓ Users can edit investments.<br>✓ Users can delete investments.<br>✓ Users can update investment values.<br>✓ Net worth updates correctly. |
| **BF8 – Property Management** | Functional Testing | ✓ Users can add properties.<br>✓ Users can edit property information.<br>✓ Users can update property values.<br>✓ Property values contribute to total net worth. |
| **BF9 – Physical Asset Management** | Functional Testing | ✓ Users can add physical assets.<br>✓ Users can edit physical assets.<br>✓ Users can update asset values.<br>✓ Physical assets contribute to total net worth. |
| **BF10 – Liability Management** | Functional Testing | ✓ Users can add liabilities.<br>✓ Users can edit liabilities.<br>✓ Users can delete liabilities.<br>✓ Liability values reduce total net worth correctly. |
| **BF11 – Historical Asset Tracking** | Database Records, Functional Testing | ✓ Every value update creates a historical record.<br>✓ Historical records remain unchanged.<br>✓ Correct date and value are stored.<br>✓ Historical data is available for graph generation. |
| **BF12 – Manual Value Updates** | Functional Testing | ✓ Users can manually update all supported assets.<br>✓ Net worth recalculates immediately.<br>✓ Historical values are stored automatically.<br>✓ Updated values are reflected throughout the application. |
| **BF13 – Responsive Interface** | Screenshots | ✓ Layout displays correctly on desktop.<br>✓ Layout displays correctly on tablet.<br>✓ Layout displays correctly on mobile.<br>✓ Navigation remains fully functional across supported devices. |

---

## Summary

### Key Points

- Each Beta Feature has measurable success criteria.
- Success criteria provide a clear benchmark for development and testing.
- Every criterion can be validated using evidence gathered during testing.
- This document establishes traceability between the proposed solution and the testing phase.

---

## Related Documents

**Previous**

06_Proposed_Solution.md

**Next**

08_Limitations.md

**Related**

06_Proposed_Solution.md

Testing/Test_Plan.md