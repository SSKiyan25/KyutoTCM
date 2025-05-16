## **PROD-0003:** Product testing - Archive Product

> **Summary:** Verify that an organization user can successfully archive an existing product.

**Preconditions:**

- User must be logged in as an organization.
- At least one active product must exist in the system.

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                                 |
| --- | ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                             |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                                       |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                                       |
| 4   | Locate an existing product in the products table.                                                                  | Verify that the product is visible in the table.                                  |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                                   |
| 6   | Click the `Archive` option from the dropdown menu.                                                                 | Verify that a confirmation dialog appears.                                        |
| 7   | Click `OK` or `Confirm` in the confirmation dialog.                                                                | Verify that the dialog closes and a success message appears.                      |
| 8   | Check the products table.                                                                                          | Verify that the archived product is no longer visible in the main products table. |

**Post-conditions:**

- The product is successfully archived.
- The archived product no longer appears in the main products table.
- The product data is retained in the system but marked as archived.
