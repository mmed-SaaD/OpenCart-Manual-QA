# Requirements Analysis

## Introduction

This document analyzes the client-provided requirements to identify the business rules, acceptance criteria, potential risks, and test priority associated with each requirement. The analysis serves as the foundation for the Requirements Traceability Matrix (RTM), test scenarios, and detailed test cases.

## Functional Requirements

### FR-001 User Registration

**Module:** Authentication

#### Description

Visitors shall be able to create a customer account by providing the required registration information.

#### Acceptance Criteria

- All required personal information must be provided.
- Unique required personal information (e.g., email) must not already exist.

#### Business Rules

- Customer accounts can only be created using a unique email address.
- Mandatory fields must be completed before form submission.

#### Potential Risks

- Duplicate account creation.
- SQL Injection attempts.
- Poor server-side input validation.
- Improper registration error handling

#### Test Priority

High 🔴

### FR-002 User Login

**Module:** Authentication

#### Description

Registered customers shall be able to log in using their email address and password.

#### Acceptance Criteria

- Registered customers can successfully authenticate using valid credentials.
- Invalid credentials are rejected.

#### Business Rules

- Customers can log into the application only if registered.
- Mandatory fields (email address and password) must be provided.

#### Potential Risks

- SQL Injection attempts.
- Poor server-side input validation.
- Improper login error handling


#### Test Priority

High 🔴

### FR-003 Logout

**Module:** Authentication

#### Description

Authenticated customers shall be able to terminate their session.

#### Acceptance Criteria

- Authenticated customers can successfully terminate their session.
- Customer is successfully redirected to the login page.
- Customer cannot navigate back to his session after its termination.

#### Business Rules

- Customers can log out only if already logged in.
- Session does not persist after termination.

#### Potential Risks

- Session still active after termination as anonymous user.
- Token remains valid after session termination.
- Browser back button allows access to authenticated pages.
- Cached sensitive pages still accessible even after logout.


#### Test Priority

High 🔴

### FR-004 Forgotten Password

**Module:** Authentication

#### Description

Registered customers shall be able to reset their password using the password recovery feature.

#### Acceptance Criteria

- Password reset instructions are sent and received via Email/Phone Number.
- Customer is able to create a new password.

#### Business Rules

- Only registered customers can reset their password.
- Email/Phone Number provided during registration must be valid and used.

#### Potential Risks

- SQL injection attempts
- Poor error handling.
- Poor server-side input validation.

#### Test Priority

High 🔴

### FR-005 Profile Management

**Module:** Customer Account

#### Description

Registered customers shall be able to update their personal information.

#### Acceptance Criteria

- Updated information is successfully changed.
- Unchanged information is kept as they are.

#### Business Rules

- Only registered customers can update their information.
- Each customer can only update his own information.
- All mandatory fields must be completed before submission.

#### Potential Risks

- SQL injection attempts.
- Cross-Site Scripting (XSS) attempts.
- Unauthorized modification of another customer's information.

#### Test Priority

High 🔴

### FR-006 Address Management

**Module:** Customer Account

#### Description

Registered customers shall be able to create, edit and delete their addresses.

#### Acceptance Criteria

- The new address is listed after creation.
- Address information is successfully changed after an update.
- The address is no longer visible after deletion.

#### Business Rules

- Only registered customers can manage their addresses.
- Each customer can only manage their own addresses.
- All mandatory fields must be completed before submission.

#### Potential Risks

- SQL injection attempts.
- Cross-Site Scripting (XSS) attempts.
- Unauthorized modification of another customer's addresses.

#### Test Priority

Medium 🟡

### FR-007 Password Management

**Module:** Customer Account

#### Description

Registered customers shall be able to change their password.

#### Acceptance Criteria

- Password is successfully changed.
- Password confirmation is enforced.

#### Business Rules

- Only registered customers can change their password.
- Each customer can only change his own password.
- All mandatory fields must be completed before submission.

#### Potential Risks

- SQL injection attempts.
- Cross-Site Scripting (XSS) attempts.
- Unauthorized modification of another customer's password.

#### Test Priority

High 🔴

### FR-008 Order History

**Module:** Customer Account

#### Description

Registered customers shall be able to view previously placed orders.

#### Acceptance Criteria

- The customer's previously placed orders are displayed.

#### Business Rules

- Each customer can only view his own order history.

#### Potential Risks

- Unauthorized access to another customer's order history.

#### Test Priority

Medium 🟡

### FR-009 Category Navigation

**Module:** Product Catalog

#### Description

Registered customers shall be able to browse products by category.

#### Acceptance Criteria

- Products belonging to the selected category are displayed.

#### Business Rules

- Only products assigned to the selected category are displayed.

#### Potential Risks

- Customers may not find products because they are assigned to an incorrect category.

#### Test Priority

Medium 🟡

### FR-010 Product Details

**Module:** Product Catalog

#### Description

Each product shall display its name, description, image, price, stock status and available options.

#### Acceptance Criteria

- All product information is displayed.

#### Business Rules

- Product information must correspond to the selected product.

#### Potential Risks

- Incomplete or inaccurate product information may affect purchasing decisions.

#### Test Priority

High 🔴

### FR-011 Product Search

**Module:** Product Catalog

#### Description

Customers shall be able to search products by keywords.

#### Acceptance Criteria

- Products can be searched using keywords.

#### Business Rules

- Search results are based on the provided search keywords.

#### Potential Risks

- Relevant products not returned in search results may affect sales.

#### Test Priority

High 🔴

### FR-012 Product Sorting

**Module:** Product Catalog

#### Description

Customers shall be able to sort products using available sorting options.

#### Acceptance Criteria

- All sorting options are functional.

#### Business Rules

- Products are sorted based on chosen option.

#### Potential Risks

- Incorrect product sorting may make product discovery more difficult.

#### Test Priority

Low 🟢

### FR-013 – Product Display Mode (Grid/List)

**Module:** Product Catalog

#### Description

Customers shall be able to choose the product display mode (Grid/List).

#### Acceptance Criteria

- Products are displayed according to the selected display mode.

#### Business Rules

- N/D

#### Potential Risks

- Products are displayed using an incorrect layout.

#### Test Priority

Low 🟢

### FR-014 – Products Per Page (Show)

**Module:** Product Catalog

#### Description

Customers shall be able to choose the number of products shown per page.

#### Acceptance Criteria

- The selected number of products is displayed per page.

#### Business Rules

- N/D

#### Potential Risks

- An incorrect number of products is displayed per page.

#### Test Priority

Low 🟢

### FR-015 Add to Cart

**Module:** Shopping Cart

#### Description

Customers shall be able to add products to the shopping cart.

#### Acceptance Criteria

- The selected product is successfully added to the shopping cart.
- Cart items count updated to the correct count.
- Product displayed in the shopping cart.

#### Business Rules

- Each added product is only displayed once in the shopping cart.
- If an already added product is added again, the count should be updated.
- A product is added to the shopping cart after validating its stock status.
- Products that are out of stock cannot be purchased unless configured otherwise.

#### Potential Risks

- Products may be added to the shopping cart despite being unavailable.
- Order totals shall be calculated automatically.

#### Test Priority

High 🔴

### FR-016 Update Quantity

**Module:** Shopping Cart

#### Description

Customers shall be able to modify product quantities.

#### Acceptance Criteria

- The shopping cart is updated with the selected quantity.
- The total price is updated accordingly.

#### Business Rules

- The requested quantity shall not exceed the available stock.
- Quantity value must be greater than 0.
- Products that are out of stock cannot be purchased unless configured otherwise.
- Order totals shall be calculated automatically.

#### Potential Risks

- Product quantity is updated while the total price remains unchanged.

#### Test Priority

High 🔴

### FR-017 Remove Products

**Module:** Shopping Cart

#### Description

Customers shall be able to remove products from the shopping cart.

#### Acceptance Criteria

- Product is successfully removed from the shopping cart.
- Shopping cart items count is updated.
- Checkout total is updated.

#### Business Rules

- N/D

#### Potential Risks

- Poor user experience.
- Customers may abandon their purchase.

#### Test Priority

Medium 🟡

### FR-018 Cart Summary

**Module:** Shopping Cart

#### Description

The shopping cart shall display product totals and the overall order total.

#### Acceptance Criteria

- The shopping cart displays each product's details (image, name, model, quantity, unit price, and total price).
- The shopping cart summary is accurate.

#### Business Rules

- N/D

#### Potential Risks

- Poor user experience.
- Customers may abandon their purchase.
- The shopping cart may display incorrect product information.

#### Test Priority

High 🔴

### FR-019 Wishlist Management

**Module:** Wishlist

#### Description

Authenticated customers shall be able to add and remove products from their wishlist.

#### Acceptance Criteria

- Products are successfully added to and removed from the customer's wishlist.
- Wishlist items count updates successfully.

#### Business Rules

- Only authenticated customers can manage their wishlist.

#### Potential Risks

- Poor user experience.
- Customers may forget products they intended to purchase, potentially affecting sales.

#### Test Priority

Medium 🟡

### FR-020 Product Comparison

**Module:** Product Comparison

#### Description

Customers shall be able to compare multiple products.

#### Acceptance Criteria

- Selected products are displayed in the comparison page.
- The compared products' details are displayed accurately.

#### Business Rules

- Only selected products are displayed in the comparison page.

#### Potential Risks

- Customers may have difficulty comparing products manually.

#### Test Priority

Low 🟢

### FR-021 Checkout Process

**Module:** Checkout

#### Description

Customers shall be able to complete the checkout process successfully.

#### Acceptance Criteria

- The customer can successfully place an order.
- Shopping cart is emptied.
- The placed order is displayed in the customer's order history.

#### Business Rules

- Checkout requires a valid customer account.

#### Potential Risks

- A non-valid customer may initiate and complete checkout process.
- Customers may be unable to complete their purchase.

#### Test Priority

High 🔴

### FR-022 Shipping Information

**Module:** Checkout

#### Description

Customers shall be able to select or create a shipping address.

#### Acceptance Criteria

- Existing shipping addresses are displayed.
- A new shipping address can be added.

#### Business Rules

- N/D

#### Potential Risks

- Customers may be unable to complete the checkout process if they cannot select or add a shipping address.

#### Test Priority

High 🔴

### FR-023 Shipping Method

**Module:** Checkout

#### Description

Customers shall be able to select an available shipping method.

#### Acceptance Criteria

- Existing shipping methods are displayed along with their pricing.
- Customer can select one of the shipping methods.
- The customer can add a comment about the order.

#### Business Rules

- Checkout total is updated automatically based on the selected shipping method.

#### Potential Risks

- Customers may be unable to complete the checkout process if they cannot select a shipping method.

#### Test Priority

High 🔴

### FR-024 Payment Method

**Module:** Checkout

#### Description

Customers shall be able to select an available payment method.

#### Acceptance Criteria

- Existing payment methods are displayed.
- Customer can select one of the payment methods.
- Customer can add a comment about the order.

#### Business Rules

- Customer must agree to the Terms & Conditions.

#### Potential Risks

- Customers may be unable to complete the checkout process if they cannot select a payment method.

#### Test Priority

High 🔴

### FR-025 Order Confirmation

**Module:** Checkout

#### Description

Customers shall receive confirmation after a successful order.

#### Acceptance Criteria

- Order summary must be accurate and include all checkout selected options.
- Checkout total must be calculated correctly (including shipping fees, taxes and VAT).
- Order confirmation must be displayed after a successful order.
- Order displayed in customer's order history with its status updated accordingly.

#### Business Rules

- N/D

#### Potential Risks

- Customers may submit duplicate orders if no order confirmation is displayed.

#### Test Priority

High 🔴

### FR-026 Contact Form

**Module:** Contact

#### Description

Visitors shall be able to submit inquiries using the contact form.

#### Acceptance Criteria

- Enquiries successfully sent with correct customer name and email.
- Store information such as location and telephone must be displayed.
- Successful submission confirmation displayed.
- Enquiries received by store owner.

#### Business Rules

- Mandatory fields must be completed before form submission.
- Enquiry must be between 10 and 3000 characters!

#### Potential Risks

- Customers may be unable to contact the store.

#### Test Priority

Medium 🟡

### FR-027 Product Reviews

**Module:** Product Reviews

#### Description

Customers shall be able to submit product reviews where permitted.

#### Acceptance Criteria

- Product review successfully sent.
- Product review submission confirmation is displayed.
- Product review received by webmaster for approval.
- Approved product reviews are displayed under the corresponding product.

#### Business Rules

- Mandatory fields must be completed before form submission.
- Review Text must be between 25 and 1000 characters!
- Reviews must be associated with the correct product.

#### Potential Risks

- Customers may not be able to submit reviews.
- Customers may be reluctant to purchase products without access to reviews.

#### Test Priority

Medium 🟡

## Non-Functional Requirements

### NFR-001

#### Description

Forms shall validate mandatory fields before submission.

#### Acceptance Criteria

- All forms can only be submitted when all mandatory fields are completed.

#### Business Rules

- N/D

#### Potential Risks

- Forms may be submitted with incomplete required information.

#### Test Priority

High 🔴

### NFR-002

#### Description

The application shall display meaningful validation and error messages.

#### Acceptance Criteria

- Validation and error messages are displayed when invalid input is submitted.
- Error messages clearly indicate the cause of the validation failure.
- Validation messages are displayed next to or associated with the corresponding input field.

#### Business Rules

- N/D

#### Potential Risks

- Users may not understand why an operation failed.
- Poor or unclear validation messages may negatively affect the user experience.

#### Test Priority

High 🔴

### NFR-003

#### Description

Navigation shall remain consistent throughout the application.

#### Acceptance Criteria

- Navigation menus are displayed consistently across all pages.
- Navigation links direct users to the correct pages.
- Navigation elements maintain a consistent layout and behavior.

#### Business Rules

- N/D

#### Potential Risks

- Inconsistent navigation may confuse users.
- Poor navigation may negatively affect the user experience.

#### Test Priority

Medium 🟡






