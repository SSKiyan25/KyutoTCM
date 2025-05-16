## **ORD-0005:** Order testing - Search Orders

> **Summary:** Verify that both users and organizations can search for specific orders using the search bar.

**Preconditions:**

- User must be logged in.
- Multiple orders must exist in the system.
- For regular users, they must have placed several orders.
- For organization users, they must have received multiple orders.

Scenario 1: Regular User Searches Their Orders

| #   | Step                                                            | Expected Behavior                                                   |
| --- | --------------------------------------------------------------- | ------------------------------------------------------------------- |
| 1   | Launch application.                                             | Verify that the home screen is shown.                               |
| 2   | Login as a regular user.                                        | Verify that the user dashboard is displayed.                        |
| 3   | Navigate to the My Orders page.                                 | Verify that the Orders page opens with a list of the user's orders. |
| 4   | Locate the search bar above the orders table/cards.             | Verify that the search bar is visible and accessible.               |
| 5   | Enter a known order number in the search bar.                   | Verify that the input is accepted.                                  |
| 6   | Press Enter or click the search button.                         | Verify that only the matching order is displayed.                   |
| 7   | Clear the search bar and enter a partial order number.          | Verify that all orders with matching partial numbers are displayed. |
| 8   | Clear the search and enter a product name from an order.        | Verify that orders containing that product are displayed.           |
| 9   | Clear the search and enter a date in the appropriate format.    | Verify that orders placed on that date are displayed.               |
| 10  | Enter a search term that doesn't match any orders.              | Verify that no results are shown or an appropriate message appears. |
| 11  | Clear the search bar completely.                                | Verify that all orders are displayed again.                         |
| 12  | Test the search functionality on both desktop and mobile views. | Verify that search works correctly in both table and card formats.  |

Scenario 2: Organization User Searches Orders

| #   | Step                                                                        | Expected Behavior                                                     |
| --- | --------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| 1   | Launch application.                                                         | Verify that the home screen is shown.                                 |
| 2   | Login as an organization user.                                              | Verify that the organization dashboard is displayed.                  |
| 3   | Navigate to the Orders page.                                                | Verify that the Orders page opens with a list of organization orders. |
| 4   | Locate the search bar above the orders table/cards.                         | Verify that the search bar is visible and accessible.                 |
| 5   | Enter a known order number in the search bar.                               | Verify that the input is accepted.                                    |
| 6   | Press Enter or click the search button.                                     | Verify that only the matching order is displayed.                     |
| 7   | Clear the search bar and enter a specific customer name.                    | Verify that orders from that customer are displayed.                  |
| 8   | Clear the search and enter a specific product name from inventory.          | Verify that orders containing that product are displayed.             |
| 9   | Clear the search and enter a specific date in the appropriate format.       | Verify that orders received on that date are displayed.               |
| 10  | Enter a search term related to order amounts (e.g., "₱500" or "500 pesos"). | Verify that orders with matching amounts are displayed.               |
| 11  | Enter a search term that doesn't match any orders.                          | Verify that no results are shown or an appropriate message appears.   |
| 12  | Clear the search bar completely.                                            | Verify that all orders are displayed again.                           |
| 13  | Test the search functionality on both desktop and mobile views.             | Verify that search works correctly in both table and card formats.    |

Scenario 3: Combined Search and Filter (For Both User Types)

| #   | Step                                                           | Expected Behavior                                                    |
| --- | -------------------------------------------------------------- | -------------------------------------------------------------------- |
| 1   | Log in and navigate to the Orders page.                        | Verify that the Orders page displays with search and filter options. |
| 2   | Apply a status filter first (e.g., "Pending").                 | Verify that only orders with that status are displayed.              |
| 3   | With the filter active, enter a search term in the search bar. | Verify that the search is applied within the filtered results.       |
| 4   | Clear the search but keep the filter active.                   | Verify that all orders with the filtered status are displayed again. |
| 5   | Enter a search term first, then apply a status filter.         | Verify that the filter is applied to the search results.             |
| 6   | Try different combinations of search terms and filters.        | Verify that all combinations work correctly to narrow down results.  |
| 7   | Clear both search and filters.                                 | Verify that all orders are displayed again.                          |

**Post-conditions:**

- Users can effectively search for orders using various search criteria.
- Search results are filtered correctly based on the entered search terms.
- Search functionality works properly in conjunction with filter options.
- Search works correctly on both desktop (table view) and mobile (card view) interfaces.
- All search operations maintain proper access controls (users see only their orders, organizations see only orders placed with them).
