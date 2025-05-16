## **ORD-0001:** Order testing - Add Order

> **Summary:** Verify that a user can successfully browse products, add items to cart, and place an order.

**Preconditions:**

- User must be logged in.
- Products with available stock must exist in the system.
- At least one product must have pre-order option enabled.

Scenario 1: Direct Order (In-Stock Products)

| #   | Step                                                              | Expected Behavior                                             |
| --- | ----------------------------------------------------------------- | ------------------------------------------------------------- |
| 1   | Launch application.                                               | Verify that the home screen is shown.                         |
| 2   | Navigate to the Products page or browse products on the homepage. | Verify that products are displayed.                           |
| 3   | Select a product with available stock.                            | Verify that the product detail page opens.                    |
| 4   | Select "Add to Cart" (Direct) purchase option.                    | Verify that the direct purchase options are displayed.        |
| 5   | Choose a variation from the available options.                    | Verify that the variation is selected.                        |
| 6   | Select a quantity (up to the maximum available stock).            | Verify that the quantity is accepted.                         |
| 7   | Attempt to select more than the available stock.                  | Verify that the system prevents exceeding available stock.    |
| 8   | Select a valid quantity and click "Add to Cart".                  | Verify that the item is added to the cart.                    |
| 9   | Navigate to the Cart page.                                        | Verify that the Cart page opens with the added item.          |
| 10  | Select the cart item by checking the checkbox.                    | Verify that the item is selected for checkout.                |
| 11  | Click the "Checkout" button.                                      | Verify that the Checkout page opens.                          |
| 12  | Select a payment method.                                          | Verify that the payment method is selected.                   |
| 13  | Click "Place Order" button.                                       | Verify that the order is processed.                           |
| 14  | Wait for order confirmation.                                      | Verify that the user is navigated to the Order Tracking page. |
| 15  | Check the order status on the tracking page.                      | Verify that the order is displayed with the correct status.   |

Scenario 2: Pre-Order Products

| #   | Step                                                              | Expected Behavior                                               |
| --- | ----------------------------------------------------------------- | --------------------------------------------------------------- |
| 1   | Launch application.                                               | Verify that the home screen is shown.                           |
| 2   | Navigate to the Products page or browse products on the homepage. | Verify that products are displayed.                             |
| 3   | Select a product with pre-order option enabled.                   | Verify that the product detail page opens.                      |
| 4   | Select "Pre-Order" purchase option.                               | Verify that the pre-order options are displayed.                |
| 5   | Choose a variation from the available options.                    | Verify that the variation is selected.                          |
| 6   | Select a quantity (at least one).                                 | Verify that the quantity is accepted.                           |
| 7   | Click "Add to Cart".                                              | Verify that the pre-order item is added to the cart.            |
| 8   | Navigate to the Cart page.                                        | Verify that the Cart page opens with the pre-order item.        |
| 9   | Select the cart item by checking the checkbox.                    | Verify that the item is selected for checkout.                  |
| 10  | Click the "Checkout" button.                                      | Verify that the Checkout page opens.                            |
| 11  | Select a payment method.                                          | Verify that the payment method is selected.                     |
| 12  | Click "Place Order" button.                                       | Verify that the order is processed.                             |
| 13  | Wait for order confirmation.                                      | Verify that the user is navigated to the Order Tracking page.   |
| 14  | Check the order status on the tracking page.                      | Verify that the pre-order is displayed with the correct status. |

Scenario 3: Multiple Items from Same Organization

| #   | Step                                                                                                     | Expected Behavior                                            |
| --- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| 1   | Add multiple items from the same organization to the cart (following steps 1-8 from previous scenarios). | Verify that multiple items are added to the cart.            |
| 2   | Navigate to the Cart page.                                                                               | Verify that the Cart page opens with multiple items.         |
| 3   | Select multiple items from the same organization by checking their checkboxes.                           | Verify that multiple items are selected for checkout.        |
| 4   | Click the "Checkout" button.                                                                             | Verify that the Checkout page opens with all selected items. |
| 5   | Complete the checkout process as in previous scenarios (steps 12-15 of Scenario 1).                      | Verify that the order is placed with all selected items.     |

**Post-conditions:**

- Order is successfully placed in the system.
- Order appears on the tracking page with correct items, quantities, and status.
- Inventory is updated appropriately (stock reduced for direct orders).
- Pre-orders are marked correctly in the system.
