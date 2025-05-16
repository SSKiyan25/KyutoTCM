## **PROD-0005:** Product testing - Search Products

> **Summary:** Verify that an organization user can search for products using the search bar.

**Preconditions:**

- User must be logged in as an organization.
- Multiple products with different names must exist in the system.

Scenario 1

| #   | Step                                                                                                               | Expected Behavior                                                                     |
| --- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                                 |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                                           |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed with a table of products.                  |
| 4   | Locate the search bar above the products table.                                                                    | Verify that the search bar is visible and available.                                  |
| 5   | Enter a known product name in the search bar.                                                                      | Verify that the input is accepted.                                                    |
| 6   | Press Enter or click the search button.                                                                            | Verify that the table updates to show only products matching the search term.         |
| 7   | Clear the search bar and enter a partial product name that should match multiple products.                         | Verify that all products with names containing the partial search term are displayed. |
| 8   | Enter a search term that doesn't match any product names.                                                          | Verify that the table shows no results or an appropriate message.                     |
| 9   | Clear the search bar completely.                                                                                   | Verify that all products are displayed again (subject to any active filters).         |

**Post-conditions:**

- The products table correctly filters products based on the entered search terms.
- The search functionality helps organization users quickly find specific products by name.
