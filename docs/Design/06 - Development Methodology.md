# Development Methodology

## Purpose

This document outlines the development methodology that will be used throughout the implementation of the Finance Platform. It explains how features will be developed, tested and refined to ensure the completed application satisfies the success criteria established during the planning phase.

---

# Introduction

Selecting an appropriate development methodology is important as it determines how software is planned, implemented and tested throughout the project.

As the Finance Platform is being developed by a single developer, an iterative development methodology has been selected. This approach allows features to be developed individually, tested immediately after implementation and refined where necessary before development continues.

By continuously evaluating progress throughout development, problems can be identified and corrected early, reducing the likelihood of defects affecting later stages of the project.

---

# Iterative Development

The Finance Platform will be developed using an iterative approach.

Rather than attempting to build the entire application before testing, development will be broken into a series of smaller iterations. Each iteration will focus on implementing a single Beta Feature or a closely related group of features.

After completing an iteration, the implemented functionality will be tested against the predefined Success Criteria. If all criteria are satisfied, development will continue to the next feature. If one or more criteria are not met, the feature will be refined and retested until the expected behaviour has been achieved.

This continuous cycle of implementation, testing and refinement helps ensure that each feature is functioning correctly before additional functionality is introduced.

---

# Development Cycle

Each iteration will follow the same development process.

```text
Plan Feature
      │
      ▼
Implement Feature
      │
      ▼
Test Against Success Criteria
      │
      ├───────────────┐
      │               │
Criteria Met?        No
      │               │
     Yes              ▼
      │        Modify / Debug
      │               │
      └───────────────┘
              │
              ▼
     Next Beta Feature
```

This cycle will continue until every Beta Feature has been successfully implemented and all corresponding success criteria have been satisfied.

---

# Development Order

To minimise dependencies between features, the application will be developed in a logical order.

The planned implementation order is:

1. User Authentication
2. Database Connectivity
3. Dashboard
4. Savings Management
5. Investment Management
6. Property Management
7. Loan Management
8. Miscellaneous Assets
9. Historical Asset Tracking
10. Manual Value Updates
11. Data Visualisation
12. Final User Interface Refinements

This order allows the core functionality of the application to be established before more advanced features are introduced.

---

# Success Criteria Driven Development

The Success Criteria document acts as the primary benchmark throughout development.

Each implemented feature will be compared against its corresponding success criteria to determine whether it has been completed successfully.

If a feature fails to satisfy any of its required criteria, further development and debugging will take place until all criteria have been achieved.

Using the success criteria throughout development ensures that implementation remains aligned with the original project objectives and provides a measurable definition of completion for every Beta Feature.

---

# Advantages of the Chosen Methodology

The iterative methodology provides several advantages for this project:

- Features can be tested immediately after implementation.
- Problems are identified earlier, making them easier to fix.
- Development remains closely aligned with the project's success criteria.
- Progress can be monitored throughout implementation.
- Completed features provide a stable foundation for future development.
- The application is continuously improved through repeated refinement.

---

# Summary

The Finance Platform will be developed using an iterative methodology in which each Beta Feature is implemented, tested against its success criteria and refined where necessary before progressing to the next stage.

By repeatedly following this cycle throughout development, the project aims to produce a stable, well-tested application that satisfies the objectives established during the planning phase while reducing the likelihood of defects remaining in the final system.

---

## Related Documents

**Previous**

05_Database_Design.md

**Next**

07_Test_Plan.md

**Related**

06_Proposed_Solution.md

07_Success_Criteria.md