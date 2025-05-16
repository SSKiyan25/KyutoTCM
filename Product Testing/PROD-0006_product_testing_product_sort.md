## **PROD-0006:** Product testing - Sort Products

> **Summary:** Verify that both organization users and regular users can sort products using their respective interfaces.

**Preconditions:**

- Multiple products with varying names, prices, and dates added must exist in the system.

Scenario 1: Organization User Sorting

| #   | Step                                                                                                               | Expected Behavior                                                         |
| --- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                     |
| 2   | Log in as an organization user.                                                                                    | Verify that the organization dashboard is displayed.                      |
| 3   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                               |
| 4   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed with a table of products.      |
| 5   | Locate the column headers in the products table with sort buttons beside them.                                     | Verify that the sort buttons are visible and clickable.                   |
| 6   | Click on the sort button beside the Product Name column header.                                                    | Verify that the table sorts products alphabetically by name (A-Z).        |
| 7   | Click on the same sort button again.                                                                               | Verify that the table sorts products in reverse alphabetical order (Z-A). |
| 8   | Click on the sort button beside the Date Added column header.                                                      | Verify that the table sorts products by date added (newest first).        |
| 9   | Click on the same sort button again.                                                                               | Verify that the table sorts products by date added (oldest first).        |
| 10  | Click on the sort button beside the Price column header (if available).                                            | Verify that the table sorts products by price (lowest first).             |
| 11  | Click on the same sort button again.                                                                               | Verify that the table sorts products by price (highest first).            |

Scenario 2: Regular User Sorting

| #   | Step                                                                                                              | Expected Behavior                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                               | Verify that the home screen is shown.                                     |
| 2   | Navigate to the Products page.                                                                                    | Verify that the Products page for regular users is displayed.             |
| 3   | Locate the sort options (usually a dropdown or buttons indicating "Price: Low to High" and "Price: High to Low"). | Verify that the sort options are visible and accessible.                  |
| 4   | Select the "Price: Low to High" option.                                                                           | Verify that products are sorted from lowest to highest price.             |
| 5   | Select the "Price: High to Low" option.                                                                           | Verify that products are sorted from highest to lowest price.             |
| 6   | If other sort options exist (like "Newest" or "Popular"), select those options.                                   | Verify that products are sorted accordingly based on the selected option. |

**Post-conditions:**

- Products are correctly sorted based on the selected sort criteria for both organization users and regular users.
- The sort functionality helps users organize products in their preferred order.
