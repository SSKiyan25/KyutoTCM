## **SET-0001:** General Settings testing - Decimal Precision

> **Summary:** Verify that the system correctly enforces a two-decimal place precision for prices and commission rates.

**Preconditions:**

- For price testing, user must be logged in as an organization.
- For commission testing, user must be logged in as an admin.
- At least one product must exist in the system for price testing.

Scenario 1: Verify Price Decimal Precision for Products and Variations

| #   | Step                                                                                                               | Expected Behavior                                                                                             |
| --- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                | Verify that the home screen is shown.                                                                         |
| 2   | For desktop, click the `Products` link in the sidebar.                                                             | Verify that the Products page is displayed.                                                                   |
| 3   | For mobile, click the `Products` link in the footer or tap the burger icon and select `Products` from the sidebar. | Verify that the Products page is displayed.                                                                   |
| 4   | Click the `Add Product` button.                                                                                    | Verify that the Add Product form is displayed.                                                                |
| 5   | Fill in the required product details (name, description, etc.).                                                    | Verify that the input is accepted.                                                                            |
| 6   | Enter a price with exactly two decimal places (e.g., "99.99").                                                     | Verify that the price is accepted and displayed correctly.                                                    |
| 7   | Try to enter a price with more than two decimal places (e.g., "99.999").                                           | Verify that the input is either automatically truncated to two decimal places or an error message is shown.   |
| 8   | Enter a price with one decimal place (e.g., "99.9").                                                               | Verify that the input is either automatically formatted to show two decimal places (99.90) or accepted as is. |
| 9   | Enter a price with no decimal places (e.g., "99").                                                                 | Verify that the input is either automatically formatted to show two decimal places (99.00) or accepted as is. |
| 10  | Save the product.                                                                                                  | Verify that the product is saved with the correct price format.                                               |
| 11  | Locate the newly created product in the products table.                                                            | Verify that the product is visible in the table with the correct price format.                                |
| 12  | Click the "more-horizontal" action button for the selected product.                                                | Verify that a dropdown menu of actions appears.                                                               |
| 13  | Click the `Manage Inventory` option from the dropdown menu.                                                        | Verify that the Manage Inventory page opens.                                                                  |
| 14  | Click the `Add Variation` button.                                                                                  | Verify that a new variation form appears.                                                                     |
| 15  | Enter variation attributes (e.g., Size: "Medium", Color: "Blue").                                                  | Verify that the input is accepted.                                                                            |
| 16  | Repeat steps 6-9 for the variation price.                                                                          | Verify that the same decimal precision rules apply to variation prices.                                       |
| 17  | Save the variation.                                                                                                | Verify that the variation is saved with the correct price format.                                             |

Scenario 2: Verify Commission Rate Decimal Precision

| #   | Step                                                                                       | Expected Behavior                                                                                             |
| --- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                                                                         |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.                                                          |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.                                                 |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.                                              |
| 5   | In the sidebar, navigate to the `Organizations` page.                                      | Verify that the Organizations page is displayed.                                                              |
| 6   | Locate the commission rate card which displays the current rate.                           | Verify that the current commission rate is visible.                                                           |
| 7   | Click the button on the commission rate card to change the rate.                           | Verify that the Set Commission Rate modal appears.                                                            |
| 8   | Enter a commission rate with exactly two decimal places (e.g., "15.75").                   | Verify that the commission rate is accepted.                                                                  |
| 9   | Try to enter a commission rate with more than two decimal places (e.g., "15.753").         | Verify that the input is either automatically truncated to two decimal places or an error message is shown.   |
| 10  | Enter a commission rate with one decimal place (e.g., "15.5").                             | Verify that the input is either automatically formatted to show two decimal places (15.50) or accepted as is. |
| 11  | Enter a commission rate with no decimal places (e.g., "15").                               | Verify that the input is either automatically formatted to show two decimal places (15.00) or accepted as is. |
| 12  | Enter remarks in the remarks field explaining the reason for the change.                   | Verify that the remarks are accepted.                                                                         |
| 13  | Click the `Save` or `Update` button.                                                       | Verify that a success message appears and modal closes.                                                       |
| 14  | Check the commission rate card on the Organizations page.                                  | Verify that it displays the updated commission rate with the correct decimal format.                          |

**Post-conditions:**

- Product prices and variation prices are consistently displayed with up to two decimal places.
- Commission rates are consistently displayed with up to two decimal places.
- The system prevents entering more than two decimal places for prices and commission rates.
- All monetary calculations in the system use the correct decimal precision.
