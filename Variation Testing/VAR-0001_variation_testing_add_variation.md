## **VAR-0001:** Variation testing - Add Variation

> **Summary:** Verify that an organization user can successfully add variations to a product through the Manage Inventory page.

**Preconditions:**

- User must be logged in as an organization.
- At least one product must already exist in the system.

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                                                                            |
| --- | ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                                                                        |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                                                                                  |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                                                                                  |
| 4   | Locate an existing product in the products table.                                                                  | Verify that the product is visible in the table.                                                                             |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                                                                              |
| 6   | Click the `Manage Inventory` option from the dropdown menu.                                                        | Verify that the Manage Inventory page opens.                                                                                 |
| 7   | Locate the Variations section on the Manage Inventory page.                                                        | Verify that the Variations section is visible.                                                                               |
| 8   | Click the `Add Variation` button.                                                                                  | Verify that a new variation form appears.                                                                                    |
| 9   | Enter variation attributes (e.g., Size: "Medium", Color: "Blue").                                                  | Verify that the input is accepted.                                                                                           |
| 10  | Enter a price for the variation (can include up to 2 decimal places).                                              | Verify that the price is accepted and correctly formatted.                                                                   |
| 11  | Enter the stock quantity (can be zero).                                                                            | Verify that the stock value is accepted.                                                                                     |
| 12  | Click the `Add Variation` button again.                                                                            | Verify that another variation form appears.                                                                                  |
| 13  | Repeat steps 9-11 to add multiple variations.                                                                      | Verify that each variation is added to the list.                                                                             |
| 14  | Attempt to add more than 10 variations.                                                                            | Verify that a message appears indicating the 10 variation limit or the Add Variation button is disabled after 10 variations. |
| 15  | Attempt to save a variation with no price.                                                                         | Verify that an error message appears indicating price is required.                                                           |
| 16  | Attempt to save a variation with an invalid price (e.g., more than 2 decimal places).                              | Verify that an error message appears or the input is automatically formatted.                                                |
| 17  | Click the `Save` or `Save Variations` button.                                                                      | Verify that a loading indicator appears.                                                                                     |
| 18  | Wait for the update process to complete.                                                                           | Verify that a success message appears.                                                                                       |
| 19  | Navigate back to the Products page.                                                                                | Verify that the product's inventory has been updated.                                                                        |
| 20  | View the product details or manage inventory again.                                                                | Verify that the product now shows the added variations.                                                                      |

**Post-conditions:**

- The product has variations added to it.
- Each variation has the correct attributes, price, and stock quantity.
- The system enforces the limitation of 10 variations per product.
- Users can select from these variations when viewing the product.
