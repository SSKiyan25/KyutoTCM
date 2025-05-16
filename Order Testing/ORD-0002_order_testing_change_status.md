## **ORD-0002:** Order testing - Change Order Status

> **Summary:** Verify that an organization user can successfully change the status of an order.

**Preconditions:**

- User must be logged in as an organization.
- At least one order must exist in the system for the organization.

Scenario 1: Change Order Status to Preparing

| #   | Step                                                             | Expected Behavior                                             |
| --- | ---------------------------------------------------------------- | ------------------------------------------------------------- |
| 1   | Launch application.                                              | Verify that the home screen is shown.                         |
| 2   | Login as an organization user.                                   | Verify that the organization dashboard is displayed.          |
| 3   | Navigate to the Orders page.                                     | Verify that the Orders page opens with a list of orders.      |
| 4   | Locate an order with status "Pending" or similar initial status. | Verify that the order is visible in the list.                 |
| 5   | Click the Actions button for the selected order.                 | Verify that a dropdown menu appears.                          |
| 6   | Navigate to Order Actions in the dropdown menu.                  | Verify that the Order Actions submenu appears.                |
| 7   | Click the "Set as Preparing" action button.                      | Verify that a confirmation dialog appears if applicable.      |
| 8   | Confirm the status change if prompted.                           | Verify that the dialog closes.                                |
| 9   | Check the status of the order.                                   | Verify that the order status has changed to "Preparing".      |
| 10  | Check if any notifications have been sent to the customer.       | Verify that appropriate notifications are sent if applicable. |

Scenario 2: Change Order Status to Ready

| #   | Step                                                       | Expected Behavior                                             |
| --- | ---------------------------------------------------------- | ------------------------------------------------------------- |
| 1   | Navigate to the Orders page as an organization user.       | Verify that the Orders page is displayed.                     |
| 2   | Locate an order with status "Preparing".                   | Verify that the order is visible in the list.                 |
| 3   | Click the Actions button for the selected order.           | Verify that a dropdown menu appears.                          |
| 4   | Navigate to Order Actions in the dropdown menu.            | Verify that the Order Actions submenu appears.                |
| 5   | Click the "Set as Ready" action button.                    | Verify that a confirmation dialog appears if applicable.      |
| 6   | Confirm the status change if prompted.                     | Verify that the dialog closes.                                |
| 7   | Check the status of the order.                             | Verify that the order status has changed to "Ready".          |
| 8   | Check if any notifications have been sent to the customer. | Verify that appropriate notifications are sent if applicable. |

Scenario 3: Change Order Status to Completed

| #   | Step                                                       | Expected Behavior                                              |
| --- | ---------------------------------------------------------- | -------------------------------------------------------------- |
| 1   | Navigate to the Orders page as an organization user.       | Verify that the Orders page is displayed.                      |
| 2   | Locate an order with status "Ready".                       | Verify that the order is visible in the list.                  |
| 3   | Click the Actions button for the selected order.           | Verify that a dropdown menu appears.                           |
| 4   | Navigate to Order Actions in the dropdown menu.            | Verify that the Order Actions submenu appears.                 |
| 5   | Click the "Set as Completed" action button.                | Verify that a confirmation dialog appears if applicable.       |
| 6   | Confirm the status change if prompted.                     | Verify that the dialog closes.                                 |
| 7   | Check the status of the order.                             | Verify that the order status has changed to "Completed".       |
| 8   | Check the inventory levels for products in the order.      | Verify that inventory is reduced accordingly.                  |
| 9   | Check if any notifications have been sent to the customer. | Verify that appropriate notifications are sent if applicable.  |
| 10  | Check if any commission calculations have been processed.  | Verify that any applicable commission is calculated correctly. |

**Post-conditions:**

- Order status is successfully changed to the new status.
- Appropriate system actions occur based on the new status (inventory updates, notifications, etc.).
- Order history accurately reflects the status changes.
