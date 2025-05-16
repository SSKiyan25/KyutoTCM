## **ORG-0006:** Organization testing - Sort Organizations

> **Summary:** Verify that an admin can sort organizations in the table by clicking on the sort buttons beside each column header.

**Preconditions:**

- User must be an admin and using a desktop/PC.
- Multiple organizations must exist in the system.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                              |
| --- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                                          |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.                           |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.                  |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.               |
| 5   | In the sidebar, navigate to the `Organizations` page.                                      | Verify that the Organizations page is displayed with a table of organizations. |
| 6   | Locate the column headers in the organizations table with sort buttons beside them.        | Verify that the sort buttons are visible and clickable.                        |
| 7   | Click on the sort button beside the Organization Name column header.                       | Verify that the table sorts organizations alphabetically by name (A-Z).        |
| 8   | Click on the same sort button again.                                                       | Verify that the table sorts organizations in reverse alphabetical order (Z-A). |
| 9   | Click on the sort button beside a different column header (e.g., Status).                  | Verify that the table sorts organizations by that column.                      |
| 10  | Click on the same sort button again.                                                       | Verify that the sort order for that column is reversed.                        |

**Post-conditions:**

- The organizations table correctly sorts based on the selected column.
- The sort buttons visually indicate the current sort direction (ascending or descending).
- The admin can efficiently organize the view of organizations by different attributes.
