## **ORD-0003:** Order testing - Order Cancellation

> **Summary:** Verify that both users and organizations can cancel orders under appropriate conditions.

**Preconditions:**

- User must be logged in with an active account.
- At least one pending order must exist in the system.
- For organization cancellation, the user must have appropriate permissions.

Scenario 1: User Cancels Pending Order

| #   | Step                                                     | Expected Behavior                                                       |
| --- | -------------------------------------------------------- | ----------------------------------------------------------------------- |
| 1   | Launch application.                                      | Verify that the home screen is shown.                                   |
| 2   | Login as a regular user.                                 | Verify that the user dashboard is displayed.                            |
| 3   | Navigate to the My Orders page.                          | Verify that the Orders page opens with a list of the user's orders.     |
| 4   | Locate a pending order (with status "Pending").          | Verify that the pending order is visible in the list.                   |
| 5   | Click on the order to view order details.                | Verify that the order details page opens.                               |
| 6   | Click the "Cancel Order" button.                         | Verify that a confirmation dialog appears.                              |
| 7   | Enter a cancellation reason to the input.                | Verify that the cancellation reason is selected.                        |
| 8   | Click "Confirm Cancellation" button.                     | Verify that the confirmation dialog closes.                             |
| 9   | Check the order status.                                  | Verify that the order status has changed to "Cancelled by User".        |
| 10  | Verify the inventory effect.                             | Verify that any reserved inventory is released back to available stock. |
| 11  | Check if any notifications are sent to the organization. | Verify that the organization receives a cancellation notification.      |
| 12  | Navigate to order history.                               | Verify that the cancelled order appears with the correct status.        |

Scenario 2: User Attempts to Cancel Order in Process

| #   | Step                                                | Expected Behavior                                                   |
| --- | --------------------------------------------------- | ------------------------------------------------------------------- |
| 1   | Navigate to the My Orders page as a regular user.   | Verify that the Orders page opens with a list of the user's orders. |
| 2   | Locate an order with status "Preparing" or "Ready". | Verify that the order is visible in the list.                       |
| 3   | Click on the order to view order details.           | Verify that the order details page opens.                           |
| 4   | Check for the presence of a "Cancel Order" button.  | Verify that the "Cancel Order" button is either disabled or absent. |
| 5   | If possible, attempt to cancel the order.           | Verify that the system prevents cancellation with an error message. |
| 6   | Check the order status.                             | Verify that the order status remains unchanged.                     |

Scenario 3: Organization Cancels Order

| #   | Step                                                        | Expected Behavior                                                        |
| --- | ----------------------------------------------------------- | ------------------------------------------------------------------------ |
| 1   | Launch application.                                         | Verify that the home screen is shown.                                    |
| 2   | Login as an organization user with order management access. | Verify that the organization dashboard is displayed.                     |
| 3   | Navigate to the Orders page.                                | Verify that the Orders page opens with a list of orders.                 |
| 4   | Locate an order (any status except "Completed").            | Verify that the order is visible in the list.                            |
| 5   | Click the Actions button for the selected order.            | Verify that a dropdown menu appears.                                     |
| 6   | Navigate to Order Actions in the dropdown menu.             | Verify that the Order Actions submenu appears.                           |
| 7   | Click the "Cancel Order" action button.                     | Verify that a confirmation dialog appears.                               |
| 8   | Enter a cancellation reason to the input.                   | Verify that the cancellation reason is selected.                         |
| 9   | Click "Confirm Cancellation" button.                        | Verify that the confirmation dialog closes.                              |
| 10  | Check the order status.                                     | Verify that the order status has changed to "Cancelled by Organization". |
| 11  | Verify the inventory effect.                                | Verify that any reserved inventory is released back to available stock.  |
| 12  | Check if any notifications are sent to the user.            | Verify that the user receives a cancellation notification.               |
| 13  | Navigate to order history.                                  | Verify that the cancelled order appears with the correct status.         |

**Post-conditions:**

- Order status is successfully changed to "Cancelled by User" or "Cancelled by Organization" as appropriate.
- Inventory originally allocated to the order is returned to available stock.
- Order history accurately reflects the cancellation details, including reason and timestamp.
- Appropriate notifications are sent to affected parties.
