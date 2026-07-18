# 05 - Product Research

## Purpose

This document investigates existing financial applications and tools to identify design principles, strengths and limitations that have influenced the development of Finance Platform. The findings from this research are used to justify design decisions made throughout the project.

---

# Introduction

Before designing Finance Platform, several existing financial products were researched to understand how they present financial information, organise data and support users in managing their wealth.

Rather than replicating existing applications, the aim of this research is to identify successful design patterns while recognising areas where improvements can be made. The products selected each represent a different approach to managing personal finances, providing a broad understanding of current solutions available to users.

---

# Research Methodology

Three products were selected for evaluation based on their popularity, intended audience and relevance to the objectives of Finance Platform.

| Product | Reason for Selection |
|----------|----------------------|
| Trading 212 | Well-designed investment platform with an intuitive dashboard and strong data presentation. |
| Emma | Personal finance application focused on accessibility and financial awareness. |
| Microsoft Excel | Widely used manual solution for tracking personal finances and wealth. |

Each product was analysed using the following criteria:

- Overall purpose
- Strengths
- Weaknesses
- Similarities with Finance Platform
- Design decisions influenced by the research

---

# Product Research

## Trading 212

### Overview

Trading 212 is an online investment platform that enables users to buy and manage stocks, ETFs and other investment products through a modern web and mobile application.

### Strengths

- Large portfolio value is immediately visible.
- Monetary and percentage changes are displayed clearly.
- Clean, modern and uncluttered interface.
- Simple navigation.
- Strong visual hierarchy that prioritises important information.

### Weaknesses

- Primarily focuses on investments rather than overall wealth.
- Candlestick charts require investment knowledge to interpret.
- Does not support tracking savings, physical assets or liabilities within a single dashboard.
- Requires users to use additional applications to understand their complete financial position.

### Similarities

Finance Platform adopts several successful design principles from Trading 212, including:

- Displaying the most important financial figure prominently.
- Showing monetary and percentage changes together.
- Using a clean, minimal interface.
- Prioritising simplicity over unnecessary visual clutter.

### Design Decisions

The research into Trading 212 influenced several key decisions.

- Net worth will become the primary focus of the dashboard rather than investment value.
- Users will be able to switch between daily, weekly, monthly and yearly changes.
- Historical performance will be displayed using a simple line graph.
- Complex financial charts such as candlestick graphs will not be included in the Beta release.

---

## Emma

### Overview

Emma is a personal finance application designed to help users understand their spending habits, budgeting and financial health by combining information from multiple accounts into a single application.

### Strengths

- Easy to understand regardless of financial experience.
- Clean and approachable interface.
- Presents financial information using simple language.
- Encourages users to regularly monitor their finances.

### Weaknesses

- Focuses primarily on budgeting and expenditure.
- Limited support for tracking broader long-term wealth.
- Does not provide detailed tracking of physical assets or manually managed investments.

### Similarities

Finance Platform shares Emma's goal of making financial information accessible to users regardless of their level of financial knowledge.

### Design Decisions

The research into Emma influenced the following decisions.

- The interface should remain approachable and easy to navigate.
- Financial terminology should be kept simple wherever possible.
- The platform should prioritise understanding over complexity.
- The dashboard should focus on clarity rather than displaying excessive information.

---

## Microsoft Excel

### Overview

Microsoft Excel is commonly used by individuals to manually record and calculate personal finances. Although it was not specifically designed for wealth management, it remains one of the most widely used financial tracking tools.

### Strengths

- Highly flexible.
- Supports unlimited customisation.
- Suitable for tracking almost any type of financial information.
- Familiar to many users.

### Weaknesses

- Manual data entry can become time-consuming.
- Calculations are created and maintained by the user.
- Difficult to visualise historical trends.
- Large spreadsheets become increasingly difficult to manage.
- Greater risk of user error.

### Similarities

Like Excel, Finance Platform allows users to manually record and manage their financial information.

### Design Decisions

Research into Excel resulted in several design decisions.

- Users will manually enter asset values during the Beta release.
- Financial calculations will be performed automatically by the application.
- Historical data will be visualised using graphs rather than spreadsheets.
- Wealth information will be organised into structured categories rather than large tables.

---

# Product Comparison

| Feature | Trading 212 | Emma | Microsoft Excel | Finance Platform (Beta) |
|----------|:-----------:|:-----:|:---------------:|:-----------------------:|
| Net Worth Overview | Partial | Partial | Manual | ✓ |
| Savings Tracking | ✗ | ✓ | ✓ | ✓ |
| Investment Tracking | ✓ | Limited | ✓ | ✓ |
| Physical Assets | ✗ | ✗ | ✓ | ✓ |
| Historical Tracking | ✓ | Limited | Manual | ✓ |
| Simple Dashboard | ✓ | ✓ | ✗ | ✓ |
| Manual Asset Entry | Limited | ✗ | ✓ | ✓ |

---

# Overall Findings

Although each product performs its intended purpose effectively, none provide a complete overview of an individual's long-term wealth.

Trading 212 provides excellent investment visualisation but is limited to investment assets.

Emma focuses on budgeting and financial awareness but does not support broader wealth tracking.

Microsoft Excel offers complete flexibility but requires significant manual effort and lacks integrated visualisation.

These findings support the need for Finance Platform, which aims to combine the strengths of each solution while addressing their individual limitations.

---

## Summary

### Key Points

- Existing applications specialise in specific areas of personal finance.
- Trading 212 influenced the overall dashboard layout and presentation.
- Emma demonstrated the importance of simplicity and accessibility.
- Microsoft Excel highlighted the benefits and limitations of manual financial tracking.
- Finance Platform combines these findings to create a centralised wealth management platform focused on understanding long-term wealth.

---

## Related Documents

**Previous**

04_Stakeholders.md

**Next**

06_Technical_Research.md

**Related**

02_Project_Vision.md

07_Proposed_Solution.md