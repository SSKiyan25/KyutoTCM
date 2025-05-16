## **ORD-0004:** Order testing - Filter Orders

> **Summary:** Verify that both users and organizations can filter orders by status (All, Pending, Preparing, Ready, Completed, or Cancelled).

**Preconditions:**

- User must be logged in.
- Multiple orders with different statuses must exist in the system.

Scenario 1: Regular User Filters Their Orders

| #   | Step                                                    | Expected Behavior                                                              |
| --- | ------------------------------------------------------- | ------------------------------------------------------------------------------ |
| 1   | Launch application.                                     | Verify that the home screen is shown.                                          |
| 2   | Login as a regular user.                                | Verify that the user dashboard is displayed.                                   |
| 3   | Navigate to the My Orders page.                         | Verify that the Orders page opens with a list of the user's orders.            |
| 4   | Locate the filter options above the orders table.       | Verify that the filter options (All, Pending, Preparing, etc.) are visible.    |
| 5   | Click on the "All" filter option (default).             | Verify that all orders for the user are displayed regardless of status.        |
| 6   | Click on the "Pending" filter option.                   | Verify that only pending orders are displayed in the table.                    |
| 7   | Check that the selected filter is visually highlighted. | Verify that the "Pending" filter appears selected/highlighted.                 |
| 8   | Click on the "Preparing" filter option.                 | Verify that only orders with "Preparing" status are displayed.                 |
| 9   | Click on the "Ready" filter option.                     | Verify that only orders with "Ready" status are displayed.                     |
| 10  | Click on the "Completed" filter option.                 | Verify that only completed orders are displayed.                               |
| 11  | Click on the "Cancelled" filter option.                 | Verify that only cancelled orders are displayed.                               |
| 12  | Click on the "All" filter option again.                 | Verify that all orders are displayed again regardless of status.               |
| 13  | Apply another filter (e.g., "Completed").               | Verify that only the filtered orders are displayed.                            |
| 14  | Check if the count of filtered orders is displayed.     | Verify that the count accurately reflects the number of filtered orders shown. |
| 15  | Refresh the page while a filter is active.              | Verify that the selected filter persists and continues to filter results.      |

Scenario 2: Organization User Filters Their Orders

| #   | Step                                                         | Expected Behavior                                                               |
| --- | ------------------------------------------------------------ | ------------------------------------------------------------------------------- |
| 1   | Launch application.                                          | Verify that the home screen is shown.                                           |
| 2   | Login as an organization user.                               | Verify that the organization dashboard is displayed.                            |
| 3   | Navigate to the Orders page.                                 | Verify that the Orders page opens with a list of orders for the organization.   |
| 4   | Locate the filter options above the orders table.            | Verify that the filter options (All, Pending, Preparing, etc.) are visible.     |
| 5   | Click on the "All" filter option (default).                  | Verify that all orders for the organization are displayed regardless of status. |
| 6   | Click on the "Pending" filter option.                        | Verify that only pending orders are displayed in the table.                     |
| 7   | Check that the selected filter is visually highlighted.      | Verify that the "Pending" filter appears selected/highlighted.                  |
| 8   | Click on the "Preparing" filter option.                      | Verify that only orders with "Preparing" status are displayed.                  |
| 9   | Click on the "Ready" filter option.                          | Verify that only orders with "Ready" status are displayed.                      |
| 10  | Click on the "Completed" filter option.                      | Verify that only completed orders are displayed.                                |
| 11  | Click on the "Cancelled" filter option.                      | Verify that only cancelled orders are displayed.                                |
| 12  | Click on the "All" filter option again.                      | Verify that all orders are displayed again regardless of status.                |
| 13  | Apply a filter (e.g., "Ready") and check for action buttons. | Verify that appropriate action buttons are available for the filtered orders.   |
| 14  | Check if the count of filtered orders is displayed.          | Verify that the count accurately reflects the number of filtered orders shown.  |

**Post-conditions:**

- Orders are correctly filtered based on the selected status filter.
- Filter selection is visually indicated to users.
- Order counts accurately reflect the filtered results.
- Filter options are consistent between user and organization views, with appropriate access controls.
