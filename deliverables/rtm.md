# Requirements Traceability Matrix (RTM)

## Introduction

This Requirements Traceability Matrix (RTM) establishes end-to-end traceability between the documented requirements, the corresponding test scenarios, and the detailed test cases prepared for the OpenCart Manual QA project.

The purpose of this document is to ensure that every functional and non-functional requirement is mapped to one or more test scenarios and executable test cases before the test execution phase begins.

---

## Traceability Matrix

| Requirement ID | Requirement Description     | Priority | Test Scenario(s) | Test Case(s)    | Mapping Status | Execution Status |
| -------------- | --------------------------- | -------- | ---------------- | --------------- | -------------- | ---------------- |
| FR-001         | User Registration           | High     | TS-001           | TC-001 – TC-004 | ✅ Prepared     | ⏳ Not Executed   |
| FR-002         | User Login                  | High     | TS-002, TS-003   | TC-005 – TC-009 | ✅ Prepared     | ⏳ Not Executed   |
| FR-003         | User Logout                 | High     | TS-004, TS-005   | TC-010 – TC-013 | ✅ Prepared     | ⏳ Not Executed   |
| FR-004         | Forgotten Password          | High     | TS-006, TS-007   | TC-014 – TC-019 | ✅ Prepared     | ⏳ Not Executed   |
| FR-005         | Profile Management          | High     | TS-008, TS-009   | TC-020 – TC-023 | ✅ Prepared     | ⏳ Not Executed   |
| FR-006         | Address Management          | Medium   | TS-010, TS-011   | TC-024 – TC-028 | ✅ Prepared     | ⏳ Not Executed   |
| FR-007         | Password Management         | High     | TS-012, TS-013   | TC-029 – TC-032 | ✅ Prepared     | ⏳ Not Executed   |
| FR-008         | Order History               | Medium   | TS-014, TS-015   | TC-033 – TC-036 | ✅ Prepared     | ⏳ Not Executed   |
| FR-009         | Category Navigation         | Medium   | TS-016           | TC-037 – TC-039 | ✅ Prepared     | ⏳ Not Executed   |
| FR-010         | Product Details             | High     | TS-017           | TC-040 – TC-042 | ✅ Prepared     | ⏳ Not Executed   |
| FR-011         | Product Search              | High     | TS-018           | TC-043 – TC-046 | ✅ Prepared     | ⏳ Not Executed   |
| FR-012         | Product Sorting             | Low      | TS-019           | TC-047 – TC-049 | ✅ Prepared     | ⏳ Not Executed   |
| FR-013         | Product Display Mode        | Low      | TS-020           | TC-050 – TC-051 | ✅ Prepared     | ⏳ Not Executed   |
| FR-014         | Products Per Page           | Low      | TS-021           | TC-052 – TC-053 | ✅ Prepared     | ⏳ Not Executed   |
| FR-015         | Add Products to Cart        | High     | TS-022, TS-023   | TC-054 – TC-058 | ✅ Prepared     | ⏳ Not Executed   |
| FR-016         | Update Cart Quantity        | High     | TS-024, TS-025   | TC-059 – TC-063 | ✅ Prepared     | ⏳ Not Executed   |
| FR-017         | Remove Products from Cart   | Medium   | TS-026           | TC-064 – TC-065 | ✅ Prepared     | ⏳ Not Executed   |
| FR-018         | Shopping Cart Summary       | High     | TS-027           | TC-066 – TC-067 | ✅ Prepared     | ⏳ Not Executed   |
| FR-019         | Wishlist                    | Medium   | TS-028, TS-029   | TC-068 – TC-071 | ✅ Prepared     | ⏳ Not Executed   |
| FR-020         | Product Comparison          | Low      | TS-030           | TC-072 – TC-074 | ✅ Prepared     | ⏳ Not Executed   |
| FR-021         | Checkout Process            | High     | TS-031, TS-032   | TC-075 – TC-078 | ✅ Prepared     | ⏳ Not Executed   |
| FR-022         | Shipping Address            | High     | TS-033           | TC-079 – TC-081 | ✅ Prepared     | ⏳ Not Executed   |
| FR-023         | Shipping Methods            | High     | TS-034           | TC-082 – TC-084 | ✅ Prepared     | ⏳ Not Executed   |
| FR-024         | Payment Methods             | High     | TS-035, TS-036   | TC-085 – TC-089 | ✅ Prepared     | ⏳ Not Executed   |
| FR-025         | Order Confirmation          | High     | TS-037, TS-038   | TC-090 – TC-094 | ✅ Prepared     | ⏳ Not Executed   |
| FR-026         | Contact Form                | Medium   | TS-039, TS-040   | TC-095 – TC-099 | ✅ Prepared     | ⏳ Not Executed   |
| FR-027         | Product Reviews             | Medium   | TS-041, TS-042   | TC-100 – TC-105 | ✅ Prepared     | ⏳ Not Executed   |
| NFR-001        | Mandatory Field Validation  | High     | TS-043           | TC-106 – TC-108 | ✅ Prepared     | ⏳ Not Executed   |
| NFR-002        | Validation & Error Messages | High     | TS-044           | TC-109 – TC-111 | ✅ Prepared     | ⏳ Not Executed   |
| NFR-003        | Consistent Navigation       | Medium   | TS-045           | TC-112 – TC-114 | ✅ Prepared     | ⏳ Not Executed   |

---

## Project Status Summary

| Metric                      |   Value |
| --------------------------- | ------: |
| Functional Requirements     |      27 |
| Non-Functional Requirements |       3 |
| Total Requirements          |      30 |
| Requirements Mapped         | 30 / 30 |
| Test Scenarios Prepared     |      45 |
| Test Cases Prepared         |     114 |
| Test Cases Executed         | 0 / 114 |
| Execution Coverage          |  **0%** |

---

## Traceability Workflow

The traceability process defined for this project is:

**Requirement → Test Scenario → Test Case → Test Execution → Defect (if applicable)**

This workflow ensures that:

* Every requirement is linked to one or more test scenarios.
* Every test scenario is supported by one or more executable test cases.
* Test execution results can be traced back to the originating requirement.
* Any defects identified during execution can be linked directly to the affected requirement.

---

## Conclusion

This RTM confirms that all documented functional and non-functional requirements have been successfully mapped to corresponding test scenarios and executable test cases.

At this stage, the test design phase has been completed, while test execution has not yet started. All test cases remain in the **Not Executed** state, and the RTM serves as the baseline for tracking execution progress, requirement verification, and defect traceability during the next phase of the project.
