## **USER-0009:** User testing - Sort Users

> **Summary:** Verify that an admin can sort users in the table by clicking on column headers in the Users page.

**Preconditions:**

- User must be an admin and using a desktop/PC.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                 |
| --- | ------------------------------------------------------------------------------------------ | ----------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                             |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.              |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.     |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.  |
| 5   | In the sidebar, navigate to the `Users` page.                                              | Verify that the Users page is displayed with the user table.      |
| 6   | Locate the column headers in the user table.                                               | Verify that column headers are visible with sorting buttons.      |
| 7   | Click on the Name/Email column header or its sorting button.                               | Verify that the table sorts users alphabetically by name (A-Z).   |
| 8   | Click on the Name/Email column header or its sorting button again.                         | Verify that the table sorts users in reverse order by name (Z-A). |

**Post-conditions:**

- The user table accurately displays users in the selected sort order.
- The sorting indicators (arrows) correctly show the current sort direction.
