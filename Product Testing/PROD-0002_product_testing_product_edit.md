## **PROD-0002:** Product testing - Edit Product

> **Summary:** Verify that an organization user can successfully edit an existing product.

**Preconditions:**

- User must be logged in as an organization.
- At least one product must already exist in the system.

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                               |
| --- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------- | --- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                           |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                                     |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                                     |
| 4   | Locate an existing product in the products table.                                                                  | Verify that the product is visible in the table.                                |
| 5   | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                                 |
| 6   | Click the `Edit` option from the dropdown menu.                                                                    | Verify that the Edit Product page opens with the product's current information. |
| 7   | Modify the product name in the Name field.                                                                         | Verify that the modified input is accepted.                                     |
| 8   | Change the selected category from the Category dropdown if desired.                                                | Verify that the new category is selected.                                       |
| 9   | Change the product status (Publish/Hidden) if desired.                                                             | Verify that the status is updated correctly.                                    |
| 10  | (Optional) Modify the product description in the Description field.                                                | Verify that the modified input is accepted.                                     |
| 11  | Toggle the pre-order checkbox if desired.                                                                          | Verify that the checkbox state is changed as expected.                          |     |
| 13  | Change the Featured Image if desired (must be under 10MB).                                                         | Verify that the new featured image upload is successful.                        |
| 14  | (Optional) Add or remove additional images (up to 5) that are under 10MB each.                                     | Verify that the image changes are applied successfully.                         |
| 15  | Click the `Save` or `Update Product` button.                                                                       | Verify that a loading indicator appears.                                        |
| 16  | Wait for the product update process to complete.                                                                   | Verify that a success message appears.                                          |
| 17  | Navigate back to the Products page.                                                                                | Verify that the product appears with the updated details.                       |

**Post-conditions:**

- The product is updated with the modified information.
- The updated product appears in the product list with the correct details.
