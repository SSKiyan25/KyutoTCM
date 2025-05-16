## **VAR-0002:** Variation testing - Edit Variation

> **Summary:** Verify that an organization user can successfully edit a variation's name and price.

**Preconditions:**

- User must be logged in as an organization.
- At least one product with at least one variation must exist in the system.

Scenario 1: Edit Variation Name

| #   | Step                                                                                                               | Expected Behavior                                                |
| --- | ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                            |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                      |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                      |
| 4   | Locate an existing product with variations in the products table.                                                  | Verify that the product is visible in the table.                 |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                  |
| 6   | Click the `Manage Inventory` option from the dropdown menu.                                                        | Verify that the Manage Inventory page opens.                     |
| 7   | Locate the Variations section and find an existing variation.                                                      | Verify that the variation is visible in the list.                |
| 8   | Locate the actions section for the selected variation.                                                             | Verify that the actions buttons are visible.                     |
| 9   | Click the `Edit Name` button for the selected variation.                                                           | Verify that a name edit dialog or form appears.                  |
| 10  | Modify the variation name or attributes (e.g., change "Medium" to "Medium-Large").                                 | Verify that the input is accepted.                               |
| 11  | Click the `Save` or `Confirm` button.                                                                              | Verify that the dialog closes and the variation name is updated. |

Scenario 2: Edit Variation Price

| #   | Step                                                                                                       | Expected Behavior                                                             |
| --- | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| 1   | Navigate to the Manage Inventory page for a product with variations (following steps 1-6 from Scenario 1). | Verify that the Manage Inventory page is displayed.                           |
| 2   | Locate the Variations section and find an existing variation.                                              | Verify that the variation is visible in the list.                             |
| 3   | Locate the actions section for the selected variation.                                                     | Verify that the actions buttons are visible.                                  |
| 4   | Click the `Change Price` button for the selected variation.                                                | Verify that a price edit dialog or form appears.                              |
| 5   | Modify the price value (must include a valid price with up to 2 decimal places).                           | Verify that the input is accepted.                                            |
| 6   | Attempt to enter an invalid price (e.g., empty or more than 2 decimal places).                             | Verify that an error message appears or the input is automatically formatted. |
| 7   | Enter a valid price value.                                                                                 | Verify that the input is accepted.                                            |
| 8   | Click the `Save` or `Confirm` button.                                                                      | Verify that the dialog closes and the variation price is updated.             |
| 9   | Check the variation list.                                                                                  | Verify that the price is displayed with the updated value.                    |

**Post-conditions:**

- Variation names and attributes can be edited successfully.
- Variation prices can be edited successfully, following the required format (up to 2 decimal places).
- All changes are saved and displayed correctly in the system.
