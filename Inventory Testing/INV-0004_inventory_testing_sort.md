## **INV-0004:** Inventory testing - Sort Inventory Logs

> **Summary:** Verify that users can sort inventory logs by different columns.

**Preconditions:**

- User must be logged in as an organization.
- At least one product with at least one variation must exist in the system.
- The variation must have multiple inventory history entries.

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                                       |
| --- | ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                                   |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                                             |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                                             |
| 4   | Locate an existing product with variations in the products table.                                                  | Verify that the product is visible in the table.                                        |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                                         |
| 6   | Click the `Manage Inventory` option from the dropdown menu.                                                        | Verify that the Manage Inventory page opens.                                            |
| 7   | Locate the Variations section and find an existing variation with multiple inventory log entries.                  | Verify that the variation is visible in the list.                                       |
| 8   | Select the variation to view its detailed inventory logs.                                                          | Verify that the inventory history table is displayed.                                   |
| 9   | Locate the column headers with sort buttons in the inventory logs table.                                           | Verify that the sort buttons are visible beside Date, Action, and Quantity columns.     |
| 10  | Click on the sort button beside the Date column.                                                                   | Verify that the table sorts entries by date (newest first).                             |
| 11  | Click on the sort button beside the Date column again.                                                             | Verify that the table sorts entries by date (oldest first).                             |
| 12  | Click on the sort button beside the Action column.                                                                 | Verify that the table sorts entries alphabetically by action type (A-Z).                |
| 13  | Click on the sort button beside the Action column again.                                                           | Verify that the table sorts entries in reverse alphabetical order by action type (Z-A). |
| 14  | Click on the sort button beside the Quantity column.                                                               | Verify that the table sorts entries by quantity (lowest first).                         |
| 15  | Click on the sort button beside the Quantity column again.                                                         | Verify that the table sorts entries by quantity (highest first).                        |

**Post-conditions:**

- Inventory log entries can be sorted by Date, Action, and Quantity.
- Sort direction toggles between ascending and descending when clicking the same column header multiple times.
- Users can easily organize inventory logs to find specific information.
