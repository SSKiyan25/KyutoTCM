## **PROD-0001:** Product testing - Add Product

> **Summary:** Verify that an organization user can successfully add a new product.

**Preconditions:**

- User must be logged in as an organization.

Scenario 1

| #   | Step                                                                                                                             | Expected Behavior                                        |
| --- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| 1   | Launch application.                                                                                                              | Verify that the home screen is shown.                    |
| 2   | For desktop, click the `Products` link in the sidebar.                                                                           | Verify that the Products page is displayed.              |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar.               | Verify that the Products page is displayed.              |
| 4   | Click the `Add Product` button.                                                                                                  | Verify that the Add Product page opens.                  |
| 5   | Enter a product name in the Name field.                                                                                          | Verify that the input is accepted.                       |
| 6   | Select a category from the Category dropdown.                                                                                    | Verify that the category is selected.                    |
| 7   | Set the product status (Publish/Hidden).                                                                                         | Verify that the status is set correctly.                 |
| 8   | (Optional) Enter a product description in the Description field.                                                                 | Verify that the input is accepted.                       |
| 9   | Check the box if the product allows pre-order.                                                                                   | Verify that the checkbox is toggled.                     |
| 10  | (Note) The Variations section allows adding up to 10 variations (Size/Color, price) but will be covered in a separate test case. | Verify awareness of the variations limit.                |
| 11  | Upload a Featured Image (required) that is under 10MB.                                                                           | Verify that the featured image upload is successful.     |
| 12  | (Optional) Upload additional images (up to 5) that are under 10MB each.                                                          | Verify that the additional images upload successfully.   |
| 13  | Click the `Add Product` button.                                                                                                  | Verify that a loading indicator appears.                 |
| 14  | Wait for the product creation process to complete.                                                                               | Verify that a success message appears.                   |
| 15  | Navigate back to the Products page.                                                                                              | Verify that the newly added product appears in the list. |

**Post-conditions:**

- The new product is added to the organization's product catalog.
- The product appears in the product list with the correct details.
