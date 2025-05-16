## **PROD-0004:** Product testing - Filter Products

> **Summary:** Verify that an organization user can filter products using the filtering tools.

**Preconditions:**

- User must be logged in as an organization.
- Multiple products with different statuses and categories must exist in the system.

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                                       |
| --- | ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                                   |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                                             |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed with a table of products.                    |
| 4   | Locate the filter tools above the products table.                                                                  | Verify that the filter options are visible.                                             |
| 5   | Click on the `Published` filter option.                                                                            | Verify that the table updates to show only published products.                          |
| 6   | Click on the `Draft` filter option.                                                                                | Verify that the table updates to show only draft products.                              |
| 7   | Click on the `Archived` filter option.                                                                             | Verify that the table updates to show only archived products.                           |
| 8   | Locate the category filter dropdown.                                                                               | Verify that the category filter is available.                                           |
| 9   | Click on the category filter dropdown and select a specific category.                                              | Verify that the table updates to show only products in that category.                   |
| 10  | Select a different category from the dropdown.                                                                     | Verify that the table updates to show products in the newly selected category.          |
| 11  | Select "All Categories" or similar option from the dropdown (if available).                                        | Verify that products from all categories are displayed (based on other active filters). |
| 12  | Click on "All" or "Reset Filters" to clear all filters (if available).                                             | Verify that all products are displayed again regardless of status or category.          |

**Post-conditions:**

- The products table correctly filters products based on the selected status and category filters.
- The organization user can easily find products by their status or category.
