## **USER-0012:** User testing - Search Products

> **Summary:** Verify that users can search for products using the search bar.

**Preconditions:**

- Application is accessible.
- Multiple products with different names exist in the system.

Scenario 1

| #   | Step                                                 | Expected Behavior                                                        |
| --- | ---------------------------------------------------- | ------------------------------------------------------------------------ |
| 1   | Launch application.                                  | Verify that the home screen is shown.                                    |
| 2   | Navigate to the Products page.                       | Verify that the Products page is displayed.                              |
| 3   | Locate the search bar on the Products page.          | Verify that the search bar is visible and accessible.                    |
| 4   | Enter a known product name in the search bar.        | Verify that the input is accepted.                                       |
| 5   | As you type, observe the overlay div that appears.   | Verify that an overlay appears showing matching products.                |
| 6   | Continue typing a complete product name.             | Verify that the overlay updates with more specific matches.              |
| 7   | Click on one of the product matches in the overlay.  | Verify that you are navigated to that product's detail page.             |
| 8   | Return to the Products page.                         | Verify that the Products page is displayed again.                        |
| 9   | Enter a partial product name in the search bar.      | Verify that the overlay shows all products containing that partial text. |
| 10  | Enter a search term that doesn't match any products. | Verify that the overlay shows a "No results found" message or similar.   |
| 11  | Clear the search bar.                                | Verify that the overlay disappears.                                      |

**Post-conditions:**

- The search functionality correctly displays matching products in an overlay.
- Users can quickly find and navigate to specific products by searching for their names.
