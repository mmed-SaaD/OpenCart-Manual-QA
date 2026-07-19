# OpenCart Manual QA Project    -   Test Strategy

### Overview

The purpose of this testing effort is to evaluate the quality, stability, and usability of the OpenCart 3.0.5.0 e-commerce application before release. The objective is to identify functional defects, usability issues, and inconsistencies that could negatively impact the customer experience during common shopping activities.

### Objectives

The testing activities aim to:

    - Verify that core business workflows function as expected.
    - Ensure users can successfully browse and purchase products.
    - Validate customer account functionality.
    - Detect functional, UI, and usability defects.
    - Assess the application's readiness for production.

### System Under Test

- Application : **OpenCart 3.0.5.0**
- Environment : **Local Docker deployment**
- Device :
    * Host Environment : Windows 11
    * Deployment : Docker
    * Browser : Microsoft Edge (latest)
    * Testing Type : Manual
- Browser : **Microsoft Edge (latest)**
- Testing Type : **Manual**
- In Scope : 
    * User registration
    * Login / Logout
    * Password recovery
    * Account management
    * Product browsing
    * Product search
    * Categories
    * Product page
    * Shopping cart
    * Wishlist
    * Product comparison
    * Checkout process
    * Contact forms
    * Customer reviews
    * Order history
    * Responsive behavior
    * Cross-browser compatibility
    * General usability and UI consistency
- Out of Scope :
    * Mobile testing
    * Tablet testing
    * Cross-browser testing
    * Performance testing
    * Security testing
    * Automation testing
    * Source code review

### Test Approach

Testing will primarily consist of :
    - Functional Testing
    - Exploratory Testing
    - Ui Testing
    - Usability Testing
    - Negative Testing Where Appropriate

### Test Design Technique

- Requirement-based Testing
- Risk-based Testing
- Exploratory Testing
- Equivalence Partitioning
- Boundary Value Analysis (where applicable)
- Error Guessing
- State Transitioning Testing

### Entry Criteria

Testing will begin once:

    - The application is successfully installed.
    - Database configuration is complete.
    - Administrator account is created.
    - Sample data is available.
    - The application is accessible through Microsoft Edge.

### Exit Criteria

Testing will be considered complete when:

    - All planned test scenarios have been executed.
    - Critical business workflows have been validated.
    - All identified defects have been documented.
    - A final QA summary has been prepared.

### Defect Severity

| Severity | Description |
|----------|-------------|
| Critical | Prevents users from completing core business workflows. |
| High | Major functionality is broken with no reasonable workaround. |
| Medium | Functionality works but behaves incorrectly or causes inconvenience. |
| Low | Cosmetic, UI, spelling, or minor usability issues. |

### Testing Window

Testing will be conducted during dedicated QA sessions using a stable local environment.

### Responsible Individual

QA engineer **Mohamed Saad B.**

### Deliverables

The following documents will be delivered by the end of this project :

    - Test Strategy
    - Test Plan
    - Requirements Analysis
    - RTM
    - Test Scenarios
    - Test Cases
    - Exploratory Testing Notes
    - Bug Reports
    - Final QA Report