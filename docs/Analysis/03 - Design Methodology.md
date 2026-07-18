# 03 - Design Methodology

## Purpose

This document outlines the software development methodology adopted for Finance Platform. It explains how the project will be planned, designed, implemented and tested throughout its development lifecycle.

---

# Introduction

Selecting an appropriate development methodology is essential to ensuring the project remains organised, maintainable and achievable. As Finance Platform is a long-term project developed alongside university studies, part-time employment and internship applications, the methodology must provide clear structure while remaining flexible enough to accommodate future improvements.

To achieve this, the project follows a **modified Waterfall methodology** combined with **iterative development**.

---

# Modified Waterfall Methodology

The project follows the traditional Waterfall phases:

1. Analysis
2. Design
3. Implementation
4. Testing
5. Review

Each phase has a defined objective before progressing to the next.

| Phase | Objective |
|--------|-----------|
| Analysis | Understand the problem and define project requirements. |
| Design | Produce the technical design and project blueprint. |
| Implementation | Develop the application one component at a time. |
| Testing | Verify that implemented functionality behaves as expected. |
| Review | Evaluate progress and identify improvements for future iterations. |

Unlike a traditional Waterfall approach, these phases are not considered completely rigid. Once implementation begins, individual components are developed, tested and refined before progressing to the next component. This allows improvements to be made throughout development without abandoning the structured planning provided by Waterfall.

This approach ensures that major architectural decisions are made before coding begins while still allowing the project to evolve naturally during implementation.

---

# Iterative Development

Although the project follows a structured lifecycle, implementation is carried out iteratively.

Rather than developing the entire application before testing, each major component follows its own development cycle.

```text
Component Planning
        ↓
Implementation
        ↓
Testing
        ↓
Review
        ↓
Refinement
```

Only once a component meets its success criteria does development continue to the next component.

This reduces debugging complexity, improves software quality and allows feedback from earlier components to influence later development.

---

# Beta Development Strategy

The Beta release focuses on delivering a stable foundation rather than a feature-complete product.

Development will follow the order below:

1. Authentication
2. Database
3. Dashboard
4. Asset Management
5. Liability Management
6. Historical Tracking
7. Analytics
8. Settings

Each component will be fully implemented and tested before work begins on the next.

---

# Advantages of this Methodology

This methodology provides several benefits for the project.

- Produces comprehensive documentation before implementation.
- Reduces the likelihood of major architectural changes during development.
- Encourages incremental progress through manageable milestones.
- Allows testing to occur continuously rather than only at the end of the project.
- Supports long-term expansion through future releases.

---

# Why This Methodology Was Chosen

A modified Waterfall methodology was selected because Finance Platform is intended to demonstrate software engineering practices as well as programming ability.

Completing the analysis and design phases before implementation establishes a clear understanding of the project's objectives, architecture and requirements. This reduces uncertainty during development and creates documentation that can be referenced throughout the project.

Combining this with iterative development provides the flexibility to improve individual components without compromising the overall project structure. This balance between planning and adaptability makes the methodology well suited to a solo developer working on a long-term project with limited available development time.

---

## Summary

### Key Points

- Finance Platform follows a modified Waterfall methodology.
- Analysis and design are completed before implementation begins.
- Individual components are developed using an iterative cycle.
- Continuous testing and refinement improve software quality.
- The methodology balances structured planning with development flexibility.

---

## Related Documents

**Previous**

02_Project_Vision.md

**Next**

04_Stakeholders.md

**Related**

01_System_Architecture.md

01_Test_Plan.md