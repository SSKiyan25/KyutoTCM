## **VAR-0003:** Variation testing - Delete Variation

> **Summary:** Verify that an organization user can successfully delete a variation from a product.

**Preconditions:**

- User must be logged in as an organization.
- At least one product with at least one variation must exist in the system.

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                     |
| --- | ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                 |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                           |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                           |
| 4   | Locate an existing product with variations in the products table.                                                  | Verify that the product is visible in the table.                      |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                       |
| 6   | Click the `Manage Inventory` option from the dropdown menu.                                                        | Verify that the Manage Inventory page opens.                          |
| 7   | Locate the Variations section and find an existing variation.                                                      | Verify that the variation is visible in the list.                     |
| 8   | Locate the actions section for the selected variation.                                                             | Verify that the actions buttons are visible.                          |
| 9   | Click the `Delete` action button for the selected variation.                                                       | Verify that a confirmation dialog appears.                            |
| 10  | Click the `Continue` or `Yes` button in the confirmation dialog.                                                   | Verify that the dialog closes.                                        |
| 11  | Check the variations list.                                                                                         | Verify that the deleted variation no longer appears in the list.      |
| 12  | (Optional) If last variation was deleted, check if product reverts to simple product without variations.           | Verify appropriate system behavior when all variations are removed.   |
| 13  | Navigate back to the Products page.                                                                                | Verify that the product still exists (without the deleted variation). |

**Post-conditions:**

- The selected variation is successfully deleted from the product.
- The product page and inventory correctly reflect the removal of the variation.
- If all variations are removed, the system handles this gracefully (either converting to a simple product or showing appropriate messaging).
