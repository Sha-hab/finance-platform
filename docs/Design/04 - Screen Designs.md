# 04 – Screen Designs

## Purpose

This document presents the proposed screen designs for the Finance Platform. The purpose of these designs is to provide a visual representation of how users will interact with the application before implementation begins.

The wireframes demonstrate the overall layout, navigation structure and placement of major interface components. They serve as a planning tool that guides development and ensures the application's interface remains consistent throughout implementation.

---

# Introduction

Designing the user interface before development allows the structure of the application to be evaluated and refined without investing time into implementation. By producing a series of wireframes, the overall usability of the application can be considered early in the development process, allowing improvements to be made before any code is written.

The wireframes contained within this document should be considered **conceptual prototypes** rather than final interface designs. Their primary purpose is to communicate the overall structure of the application rather than define its final appearance.

As development progresses, aspects such as colours, spacing, typography, icons, tables and graphs may be refined. However, the overall layout and navigation philosophy established within these designs are expected to remain consistent throughout the project.

The proposed layouts have been discussed with the project stakeholders, who agreed that the overall design is intuitive, well organised and appropriate for a personal finance management platform.

---

# Design Objectives

The screen designs have been created around several key objectives.

- Maintain a consistent layout throughout the application.
- Provide a simple and intuitive navigation system.
- Reduce unnecessary clutter.
- Ensure important financial information is immediately visible.
- Clearly distinguish positive and negative financial performance.
- Create a layout that can easily be expanded as new functionality is added.
- Ensure every major feature is accessible within as few interactions as possible.

These objectives help create an interface that is easy to learn while remaining efficient for regular use.

---

# Design Philosophy

A major design decision made during planning was to maintain a **consistent interface across every page**.

Rather than designing a completely different layout for each financial category, almost every page follows the same overall structure. This allows users to become familiar with the interface quickly and navigate confidently between different sections without needing to relearn how each page operates.

The only exception to this principle is the authentication screen, where navigation options are intentionally hidden until the user has successfully logged into the application.

Every primary screen follows the same general layout consisting of:

- Application header
- Current page title
- Main content area
- User panel
- Navigation panel

Maintaining this consistency improves usability, reduces the learning curve for new users and creates a more professional appearance throughout the application.

---

# Standard Layout

Every primary screen follows the same overall layout.

The application is divided into two main sections.

The **left-hand side** contains the primary content for the selected page. This is where users interact with their financial information, view graphs, manage assets and perform the majority of system functionality.

The **right-hand side** contains a permanent navigation panel. This panel includes the current user's information, a logout button and links to every major section of the application. Keeping navigation visible at all times allows users to move throughout the application quickly without needing to return to a homepage.

At the top of every page is the application header, with the Settings button positioned in the upper-right corner where users would naturally expect to find account options.

This layout has been adopted across every financial category to maximise consistency.

---

# Colour Scheme

The application intentionally uses a minimal colour palette.

Green has been selected as the application's primary colour and is used throughout the interface for:

- headings
- navigation
- buttons
- interface highlights
- positive financial changes
- increases in value
- profits

Using a single primary colour creates consistency throughout the application while avoiding unnecessary visual clutter.

Negative financial performance is represented using **red**.

Red is reserved exclusively for information requiring the user's attention, including:

- losses
- decreases in asset values
- reductions in overall net worth
- negative daily performance

Restricting the use of red ensures that poor financial performance immediately stands out without overwhelming the user.

---

# Wireframe Development

During the planning stage, multiple hand-drawn wireframes were produced to rapidly explore different interface layouts.

Creating rough sketches before implementation allowed different ideas to be evaluated quickly without spending unnecessary time producing high-fidelity designs. This made it easier to refine the navigation structure, reposition interface components and incorporate stakeholder feedback throughout the planning process.

The wireframes shown within this document **are not final interface designs**.

Instead, they should be viewed as design guidelines that communicate:

- overall page layout
- navigation structure
- placement of major interface components
- relationship between different pages
- overall user experience

Throughout implementation, visual improvements may be made where appropriate. However, the overall page structure established within these wireframes is expected to remain largely unchanged.

---

# Dashboard

The dashboard was the first screen designed during planning and acts as the application's homepage after a successful login.

Its purpose is to provide users with an immediate overview of their financial position without requiring navigation into individual asset categories.

The dashboard currently includes:

- Total Net Worth
- Daily monetary change
- Daily percentage change
- Wealth Distribution chart
- Recent Activity feed
- User panel
- Navigation panel

Displaying this information together allows users to quickly understand both their current financial position and any recent changes.

The dashboard underwent several revisions before reaching its current layout. Earlier versions focused on determining which information should be displayed, while later revisions refined the navigation layout and improved overall consistency.

**Figure 1 – Initial Dashboard Wireframe**

*![Initial Dashboard Wireframe](<Screenshot 2026-07-28 184420.png>)*

The initial dashboard explored different arrangements of the application's key information, including total net worth, recent activity and wealth distribution.

Following discussion with stakeholders, several improvements were identified.

---

**Figure 2 – Revised Dashboard Wireframe**

*![Revised Dashboard Wireframe](<Screenshot 2026-07-30 171022.png>)*

The revised dashboard introduced several improvements, including:

- Settings relocated to the upper-right corner.
- User information and navigation combined into a single right-hand panel.
- Left-hand side reserved exclusively for page content.
- Improved spacing and organisation.
- Consistent layout adopted for future pages.
- Green selected as the primary interface colour.
- Red reserved exclusively for negative financial performance.

Stakeholders agreed that this revision provided a cleaner, more intuitive interface and should become the standard layout used throughout the application.

---

# Login Screen

Unlike the rest of the application, the login screen intentionally uses a simplified layout.

Since users have not yet authenticated, navigation options are hidden until login has been completed.

The login screen contains:

- Email field
- Password field
- Forgot Email option
- Forgot Password option
- Create Account option

A preview of the application dashboard is also displayed to provide first-time users with an indication of what they can expect after logging into the application.

**Figure 3 – Login Screen Wireframe**

*![Login Screen Wireframe](<Screenshot 2026-07-30 173641.png>)*

---

# Addtional Screens

The rest of the pages are designed using the same established layout as the dashboard, yet are also very similar to each other with minor differnces such as an additional category (weight) for precious materials.
Therfore, all of these screens have only one draft as it encompasses them all.

This page allows users to manage savings accounts held across different financial institutions.

Information displayed includes:

- Bank / Item
- Account
- Balance / Value
- Weight
- Last Updated
- Notes

Maintaining the same layout allows users to immediately understand how to manage their savings without learning a new interface.


**Figure 4 – General Screen Wireframe**

*![General Screen Wireframe](<Screenshot 2026-07-30 182133.png>)*

---

# Future Improvements

Although these wireframes represent the current design direction, they remain conceptual prototypes.

During implementation, the following aspects may be refined:

- typography
- spacing
- icons
- graphs
- tables
- animations
- responsive layouts
- accessibility improvements
- component styling

These refinements will improve the application's appearance without significantly altering the overall structure established during the design phase.

---

# Summary

The screen designs establish the visual foundation of the Finance Platform before implementation begins.

By maintaining a consistent layout across every page, users will be able to navigate the application confidently while requiring minimal time to become familiar with its interface.

Although the wireframes are not intended to represent the final appearance of the application, they successfully communicate the proposed layout, navigation structure and overall user experience. The designs have been reviewed with stakeholders and will act as the primary reference throughout the implementation phase while remaining flexible enough to accommodate future refinements.

---

## Related Documents

**Previous**

03_Technical_Design.md

**Next**

05_Database_Design.md

**Related**

01_System_Decomposition.md

02_Asset_Management_Decomposition.md

06_Proposed_Solution.md