## **USER-0011:** User testing - Filter Products

> **Summary:** Verify that users can filter products on the homepage and products page.

**Preconditions:**

- Application is accessible.
- Products of various categories and popularity exist in the system.

Scenario 1

| #   | Step                                                                       | Expected Behavior                                                          |
| --- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| 1   | Launch application.                                                        | Verify that the home screen is shown.                                      |
| 2   | On the homepage, locate the filter buttons (All, New, Popular, Top-Sales). | Verify that the filter buttons are visible.                                |
| 3   | Click on the `New` filter button.                                          | Verify that the product display updates to show only new products.         |
| 4   | Click on the `Popular` filter button.                                      | Verify that the product display updates to show only popular products.     |
| 5   | Click on the `Top-Sales` filter button.                                    | Verify that the product display updates to show only top-selling products. |
| 6   | Click on the `All` filter button.                                          | Verify that all products are displayed again.                              |
| 7   | Locate the category filter buttons.                                        | Verify that category filter options are visible.                           |
| 8   | Click on a specific category filter button.                                | Verify that only products from that category are displayed.                |
| 9   | Click on a different category filter button.                               | Verify that only products from the newly selected category are displayed.  |
| 10  | Navigate to the Products page.                                             | Verify that the Products page is displayed.                                |
| 11  | Repeat steps 2-9 on the Products page.                                     | Verify that filtering works the same way on the Products page.             |

**Post-conditions:**

- Products are correctly filtered based on the selected filter options.
- Users can easily find products by category, newness, popularity, and sales performance.
