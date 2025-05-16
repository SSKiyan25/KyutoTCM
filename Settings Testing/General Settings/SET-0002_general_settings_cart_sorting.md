## **SET-0002:** General Settings testing - Cart Sorting and Selection

> **Summary:** Verify that cart items are properly sorted by organization and the selection behavior correctly groups items from the same organization.

**Preconditions:**

- User must be logged in.
- Cart must contain items from multiple organizations.

Scenario 1: Cart Sorting by Organization

| #   | Step                                                             | Expected Behavior                                                               |
| --- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| 1   | Launch application.                                              | Verify that the home screen is shown.                                           |
| 2   | Add products from multiple organizations to cart.                | Verify that the items are added to the cart.                                    |
| 3   | Navigate to the Cart page.                                       | Verify that the Cart page is displayed.                                         |
| 4   | Observe the arrangement of cart items.                           | Verify that cart items are grouped and sorted by organization.                  |
| 5   | Check if there are any visual indicators of organization groups. | Verify that there are clear visual separators or headers for each organization. |

Scenario 2: Cart Item Selection by Organization

| #   | Step                                                                                                            | Expected Behavior                                                                                     |
| --- | --------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| 1   | Launch application and navigate to the Cart page with items from multiple organizations.                        | Verify that the Cart page is displayed with items grouped by organization.                            |
| 2   | Select (click checkbox) for an item from Organization A.                                                        | Verify that the item is selected.                                                                     |
| 3   | Observe the behavior of other items' checkboxes.                                                                | Verify that only other items from Organization A become selectable.                                   |
| 4   | Attempt to select an item from Organization B while having an item from Organization A selected.                | Verify that the item from Organization B cannot be selected or triggers a clear warning/notification. |
| 5   | Deselect all items from Organization A.                                                                         | Verify that all items are deselected.                                                                 |
| 6   | Now select an item from Organization B.                                                                         | Verify that the item is selected and only other items from Organization B become selectable.          |
| 7   | Attempt to select all items using a "Select All" checkbox if available.                                         | Verify that only items from the same organization as currently selected items are selected.           |
| 8   | Deselect all items.                                                                                             | Verify that all items are deselected.                                                                 |
| 9   | Try accessing the checkout process with items from multiple organizations selected (if possible to force this). | Verify that the system prevents checkout with mixed organizations or displays appropriate error.      |

Scenario 3: Visual Indicators for Cart Organization Grouping

| #   | Step                                                              | Expected Behavior                                                                                           |
| --- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| 1   | Navigate to the Cart page with items from multiple organizations. | Verify that the Cart page is displayed with items grouped by organization.                                  |
| 2   | Check for organization name headers or labels.                    | Verify that each organization group has a clearly visible name or identifier displayed.                     |
| 3   | Look for visual separators between organization groups.           | Verify that there are clear visual dividers between items from different organizations.                     |
| 4   | Observe any visual cues when selecting items.                     | Verify that there are visual indicators showing which organization's items are currently active/selectable. |
| 5   | Check if there's any instruction or hint text.                    | Verify that the user is informed that they can only select items from one organization at a time.           |

**Post-conditions:**

- Cart items are consistently grouped and sorted by organization.
- Users can only select and proceed to checkout with items from a single organization at a time.
- The user interface provides clear visual guidance about the organization grouping and selection constraints.
- The checkout process only processes items from a single organization in one transaction.
