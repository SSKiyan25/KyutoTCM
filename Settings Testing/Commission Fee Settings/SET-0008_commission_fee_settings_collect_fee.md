<!-- filepath: c:\projects\KyutoTCM\Settings Testing\Commission Fee Settings\SET-0008_commission_fee_settings_collect_fee.md -->

## **SET-0008:** Commission Fee Settings testing - Record Payment

> **Summary:** Verify that an admin can record commission fee payments from organizations and that these payments are properly reflected in the history logs.

**Preconditions:**

- User must be logged in as an admin.
- At least one organization with pending commission fees must exist in the system.

Scenario 1: Record Commission Fee Payment

| #   | Step                                                                                       | Expected Behavior                                                            |
| --- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                                        |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.                         |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.                |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.             |
| 5   | In the sidebar, navigate to the `Organizations` page.                                      | Verify that the Organizations page is displayed.                             |
| 6   | Locate a specific organization in the list.                                                | Verify that the organization is visible in the list.                         |
| 7   | Click the "more-horizontal" action button for the selected organization.                   | Verify that a dropdown menu of actions appears.                              |
| 8   | Click the `Manage Fees` option from the dropdown menu.                                     | Verify that the system navigates to the organization's commission fees page. |
| 9   | Review the commission history and current balance.                                         | Verify that the commission history and balance information is displayed.     |
| 10  | Click the `+ Record Payment` button.                                                       | Verify that the Record Payment modal appears.                                |
| 11  | Enter the payment amount (e.g., "1000").                                                   | Verify that the amount is accepted.                                          |
| 12  | Select or enter the payment date.                                                          | Verify that the payment date is accepted.                                    |
| 13  | Select a payment method (e.g., "Cash", "Bank Transfer").                                   | Verify that the payment method is selected.                                  |
| 14  | Enter remarks about the payment (e.g., "May 2025 commission payment").                     | Verify that the remarks are accepted.                                        |
| 15  | Click the `Save` or `Record Payment` button.                                               | Verify that a loading indicator appears.                                     |
| 16  | Wait for the save operation to complete.                                                   | Verify that a success message appears and modal closes.                      |
| 17  | Check the commission history table.                                                        | Verify that the newly recorded payment appears in the history.               |
| 18  | Verify the payment details in the history.                                                 | Verify that all entered details (amount, date, method, remarks) are correct. |
| 19  | Check the updated commission balance if applicable.                                        | Verify that the balance is updated to reflect the payment.                   |

Scenario 2: Input Validation for Payment Recording

| #   | Step                                                                                       | Expected Behavior                                                           |
| --- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| 1   | Navigate to the Record Payment modal as in steps 1-10 from Scenario 1.                     | Verify that the Record Payment modal appears.                               |
| 2   | Leave the amount field empty and try to save.                                              | Verify that an error message appears indicating amount is required.         |
| 3   | Enter an invalid amount (e.g., negative value, zero, or non-numeric characters).           | Verify that an error message appears indicating invalid amount format.      |
| 4   | Enter a valid amount but leave the payment date empty.                                     | Verify that an error message appears indicating date is required.           |
| 5   | Enter a valid amount and date but leave the payment method unselected.                     | Verify that an error message appears indicating payment method is required. |
| 6   | Enter valid values for all required fields and click `Record Payment`.                     | Verify that the payment is successfully recorded.                           |
| 7   | Check if the system prevents recording duplicate payments (same amount/date/organization). | Verify that the system either prevents duplicates or warns about them.      |

Scenario 3: Payment History Filtering and Sorting

| #   | Step                                                                                 | Expected Behavior                                                                |
| --- | ------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------- |
| 1   | Navigate to the organization's commission fees page as in steps 1-8 from Scenario 1. | Verify that the commission history is displayed.                                 |
| 2   | If available, use date filters to view payments from a specific period.              | Verify that the history displays only payments from the selected period.         |
| 3   | If available, use payment method filters to view specific types of payments.         | Verify that the history displays only payments with the selected method.         |
| 4   | If available, click on column headers to sort by date.                               | Verify that the payments sort correctly by date in ascending/descending order.   |
| 5   | If available, click on column headers to sort by amount.                             | Verify that the payments sort correctly by amount in ascending/descending order. |
| 6   | If available, use a search function to find payments with specific remarks.          | Verify that only payments with matching remarks are displayed.                   |

**Post-conditions:**

- The commission fee payment is successfully recorded in the system.
- The payment appears in the organization's commission history logs with correct details.
- The organization's commission balance is updated to reflect the payment.
- The payment history can be filtered and sorted for easier review.
