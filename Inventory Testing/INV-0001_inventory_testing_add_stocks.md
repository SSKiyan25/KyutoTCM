## **INV-0001:** Inventory testing - Add Stocks

> **Summary:** Verify that an organization user can successfully add stocks to a variation.

**Preconditions:**

- User must be logged in as an organization.
- At least one product with at least one variation must exist in the system.

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                 |
| --- | ------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                             |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                       |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                       |
| 4   | Locate an existing product with variations in the products table.                                                  | Verify that the product is visible in the table.                  |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                   |
| 6   | Click the `Manage Inventory` option from the dropdown menu.                                                        | Verify that the Manage Inventory page opens.                      |
| 7   | Locate the Variations section and find an existing variation.                                                      | Verify that the variation is visible in the list.                 |
| 8   | Note the current stock level for the selected variation.                                                           | Verify that the current stock quantity is displayed.              |
| 9   | Locate the actions section for the selected variation.                                                             | Verify that the actions buttons are visible.                      |
| 10  | Click the `Add Stocks` action button for the selected variation.                                                   | Verify that a dialog or form for adding stocks appears.           |
| 11  | Enter a quantity of stocks to add (e.g., 10).                                                                      | Verify that the input is accepted.                                |
| 12  | Click the `Confirm` or `Add` button.                                                                               | Verify that the dialog closes.                                    |
| 13  | Check the stock level for the variation.                                                                           | Verify that the stock quantity has increased by the amount added. |
| 14  | Navigate back to the Products page.                                                                                | Verify that the product's inventory has been updated.             |

**Post-conditions:**

- The selected variation's stock level is successfully increased.
- The inventory changes are correctly reflected in the system.
- The product is available for purchase with the updated stock quantity.
