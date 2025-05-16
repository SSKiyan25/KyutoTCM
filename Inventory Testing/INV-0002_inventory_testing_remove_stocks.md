## **INV-0002:** Inventory testing - Remove Stocks

> **Summary:** Verify that stocks can be removed manually or automatically according to order status.

**Preconditions:**

- User must be logged in as an organization.
- At least one product with at least one variation must exist in the system.
- The variation must have stocks available.

Scenario 1: Manual Stock Removal

| #   | Step                                                                                                               | Expected Behavior                                                        |
| --- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                    |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                              |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                              |
| 4   | Locate an existing product with variations in the products table.                                                  | Verify that the product is visible in the table.                         |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                          |
| 6   | Click the `Manage Inventory` option from the dropdown menu.                                                        | Verify that the Manage Inventory page opens.                             |
| 7   | Locate the Variations section and find an existing variation with available stock.                                 | Verify that the variation is visible in the list.                        |
| 8   | Note the current stock level for the selected variation.                                                           | Verify that the current stock quantity is displayed.                     |
| 9   | Locate the actions section for the selected variation.                                                             | Verify that the actions buttons are visible.                             |
| 10  | Click the `Remove Stocks` action button for the selected variation.                                                | Verify that a dialog or form for removing stocks appears.                |
| 11  | Enter a quantity of stocks to remove (e.g., 5) that is less than the current stock level.                          | Verify that the input is accepted.                                       |
| 12  | Click the `Confirm` or `Remove` button.                                                                            | Verify that the dialog closes.                                           |
| 13  | Check the stock level for the variation.                                                                           | Verify that the stock quantity has decreased by the amount removed.      |
| 14  | Navigate back to the Remove Stocks dialog for the same variation.                                                  | Verify that the dialog appears again.                                    |
| 15  | Enter a quantity of stocks to remove that exceeds the current stock level.                                         | Verify that an error message appears or the system prevents the removal. |
| 16  | Close the dialog without confirming.                                                                               | Verify that the stock level remains unchanged.                           |

Scenario 2: Automatic Stock Removal on Order Completion

| #   | Step                                                                                                | Expected Behavior                                                                   |
| --- | --------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                 | Verify that the home screen is shown.                                               |
| 2   | Login as an organization and navigate to the Orders page.                                           | Verify that the Orders page is displayed.                                           |
| 3   | Find an order with pending status that includes variations with available stock.                    | Verify that the order details are visible.                                          |
| 4   | Note the variations and quantities in the order.                                                    | Verify that the order items are displayed correctly.                                |
| 5   | Note the current stock levels for each variation in the order.                                      | Verify that the initial stock levels are recorded.                                  |
| 6   | Mark the order status as `Completed`.                                                               | Verify that the order status is updated.                                            |
| 7   | Navigate to the Products page and access the Manage Inventory for one of the products in the order. | Verify that the Manage Inventory page is displayed.                                 |
| 8   | Check the stock levels for the variations that were in the completed order.                         | Verify that stock levels have been automatically reduced by the ordered quantities. |

**Post-conditions:**

- Stock levels can be manually reduced through the Manage Inventory interface.
- The system prevents removing more stocks than are available.
- Stock levels are automatically reduced when orders are marked as completed.
- Inventory is accurately maintained across all operations.
