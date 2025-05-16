## **INV-0003:** Inventory testing - Search Inventory Logs

> **Summary:** Verify that users can search through inventory logs for a specific variation.

**Preconditions:**

- User must be logged in as an organization.
- At least one product with at least one variation must exist in the system.
- The variation must have some inventory history (additions/removals).

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                          |
| --- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                      |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                                |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                                |
| 4   | Locate an existing product with variations in the products table.                                                  | Verify that the product is visible in the table.                           |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                            |
| 6   | Click the `Manage Inventory` option from the dropdown menu.                                                        | Verify that the Manage Inventory page opens.                               |
| 7   | Locate the Variations section and find an existing variation with inventory history.                               | Verify that the variation is visible in the list.                          |
| 8   | Select the variation to view its detailed inventory logs.                                                          | Verify that the inventory history table is displayed.                      |
| 9   | Locate the search bar above the inventory logs table.                                                              | Verify that the search bar is visible and accessible.                      |
| 10  | Enter a search term related to a known inventory change (e.g., date, quantity, or action type).                    | Verify that the input is accepted.                                         |
| 11  | Press Enter or click the search button.                                                                            | Verify that the table updates to show only matching log entries.           |
| 12  | Enter a search term that doesn't match any inventory logs.                                                         | Verify that the table shows no results or displays an appropriate message. |
| 13  | Clear the search bar.                                                                                              | Verify that all inventory logs are displayed again.                        |

**Post-conditions:**

- Users can search through inventory logs for a specific variation.
- Search results are filtered correctly based on the entered search terms.
- Users can easily find specific inventory changes in the history.
