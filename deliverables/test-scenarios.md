# Test Scenarios

## Introduction

This document defines the high-level test scenarios derived from the functional and non-functional requirements identified for the OpenCart application. These scenarios provide an overview of the areas to be tested and serve as the foundation for creating detailed test cases and the Requirements Traceability Matrix (RTM).

## Authentication

| Scenario ID | Requirement ID | Test Scenario                                                                          | Priority |
| ----------- | -------------- | -------------------------------------------------------------------------------------- | -------- |
| TS-001      | FR-001         | Verify customer registration using valid, invalid, missing and duplicate information.  | High 🔴  |
| TS-002      | FR-002         | Verify customer login using valid and invalid credentials.                             | High 🔴  |
| TS-003      | FR-002         | Verify mandatory-field validation and error handling during login.                     | High 🔴  |
| TS-004      | FR-003         | Verify logout functionality and session termination.                                   | High 🔴  |
| TS-005      | FR-003         | Verify that authenticated pages cannot be accessed after logout.                       | High 🔴  |
| TS-006      | FR-004         | Verify the forgotten-password process for registered and unregistered email addresses. | High 🔴  |
| TS-007      | FR-004         | Verify password reset instructions and new-password creation.                          | High 🔴  |

## Customer Account

| Scenario ID | Requirement ID | Test Scenario                                                                       | Priority  |
| ----------- | -------------- | ----------------------------------------------------------------------------------- | --------- |
| TS-008      | FR-005         | Verify that customers can view and update their personal information.               | High 🔴   |
| TS-009      | FR-005         | Verify profile validation and prevention of unauthorized profile modifications.     | High 🔴   |
| TS-010      | FR-006         | Verify that customers can create, edit and delete their addresses.                  | Medium 🟡 |
| TS-011      | FR-006         | Verify address validation and prevention of unauthorized address modifications.     | Medium 🟡 |
| TS-012      | FR-007         | Verify customer password change using valid and invalid information.                | High 🔴   |
| TS-013      | FR-007         | Verify authentication using the new and previous passwords after a password change. | High 🔴   |
| TS-014      | FR-008         | Verify that customers can view their previously placed orders.                      | Medium 🟡 |
| TS-015      | FR-008         | Verify that customers cannot access another customer's order history.               | Medium 🟡 |

## Product Catalog

| Scenario ID | Requirement ID | Test Scenario                                                                            | Priority  |
| ----------- | -------------- | ---------------------------------------------------------------------------------------- | --------- |
| TS-016      | FR-009         | Verify product browsing and navigation through available categories.                     | Medium 🟡 |
| TS-017      | FR-010         | Verify that the product details page displays complete and accurate product information. | High 🔴   |
| TS-018      | FR-011         | Verify product search using valid, partial, invalid and empty keywords.                  | High 🔴   |
| TS-019      | FR-012         | Verify product sorting using all available sorting options.                              | Low 🟢    |
| TS-020      | FR-013         | Verify switching between Grid and List product display modes.                            | Low 🟢    |
| TS-021      | FR-014         | Verify the selection of the number of products displayed per page.                       | Low 🟢    |

## Shopping Cart

| Scenario ID | Requirement ID | Test Scenario                                                                             | Priority  |
| ----------- | -------------- | ----------------------------------------------------------------------------------------- | --------- |
| TS-022      | FR-015         | Verify adding available, unavailable and configurable products to the shopping cart.      | High 🔴   |
| TS-023      | FR-015         | Verify shopping-cart behavior when the same product is added more than once.              | High 🔴   |
| TS-024      | FR-016         | Verify updating product quantities using valid and invalid values.                        | High 🔴   |
| TS-025      | FR-016         | Verify that product totals and the overall cart total are updated after quantity changes. | High 🔴   |
| TS-026      | FR-017         | Verify removing products from the shopping cart.                                          | Medium 🟡 |
| TS-027      | FR-018         | Verify that the shopping-cart summary displays accurate product information and totals.   | High 🔴   |

## Wishlist and Product Comparison

| Scenario ID | Requirement ID | Test Scenario                                                                        | Priority  |
| ----------- | -------------- | ------------------------------------------------------------------------------------ | --------- |
| TS-028      | FR-019         | Verify adding and removing products from an authenticated customer's wishlist.       | Medium 🟡 |
| TS-029      | FR-019         | Verify wishlist behavior for unauthenticated visitors and duplicate products.        | Medium 🟡 |
| TS-030      | FR-020         | Verify adding, displaying, comparing and removing products from the comparison list. | Low 🟢    |

## Checkout

| Scenario ID | Requirement ID | Test Scenario                                                                                                      | Priority |
| ----------- | -------------- | ------------------------------------------------------------------------------------------------------------------ | -------- |
| TS-031      | FR-021         | Verify the complete checkout process from the shopping cart to successful order placement.                         | High 🔴  |
| TS-032      | FR-021         | Verify checkout behavior for empty carts and unauthenticated customers according to the configured checkout rules. | High 🔴  |
| TS-033      | FR-022         | Verify the selection and creation of shipping addresses during checkout.                                           | High 🔴  |
| TS-034      | FR-023         | Verify the display and selection of available shipping methods and the related total calculation.                  | High 🔴  |
| TS-035      | FR-024         | Verify the display and selection of available payment methods.                                                     | High 🔴  |
| TS-036      | FR-024         | Verify Terms and Conditions acceptance and order-comment functionality during checkout.                            | High 🔴  |
| TS-037      | FR-025         | Verify the accuracy of the final order summary and calculated checkout total.                                      | High 🔴  |
| TS-038      | FR-025         | Verify order confirmation, order-history creation and duplicate-order prevention.                                  | High 🔴  |

## Contact and Product Reviews

| Scenario ID | Requirement ID | Test Scenario                                                                             | Priority  |
| ----------- | -------------- | ----------------------------------------------------------------------------------------- | --------- |
| TS-039      | FR-026         | Verify contact-form submission using valid, invalid and missing information.              | Medium 🟡 |
| TS-040      | FR-026         | Verify enquiry character limits, submission confirmation and delivery to the store owner. | Medium 🟡 |
| TS-041      | FR-027         | Verify product-review submission using valid, invalid and missing information.            | Medium 🟡 |
| TS-042      | FR-027         | Verify review character limits, approval workflow and display under the correct product.  | Medium 🟡 |

## Non-Functional Requirements

| Scenario ID | Requirement ID | Test Scenario                                                                                            | Priority  |
| ----------- | -------------- | -------------------------------------------------------------------------------------------------------- | --------- |
| TS-043      | NFR-001        | Verify mandatory-field validation across the application's main forms.                                   | High 🔴   |
| TS-044      | NFR-002        | Verify that clear and meaningful validation and error messages are displayed throughout the application. | High 🔴   |
| TS-045      | NFR-003        | Verify consistent navigation layout, links and behavior throughout the application.                      | Medium 🟡 |
