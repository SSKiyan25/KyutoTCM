## **USER-0007:** User testing - Filter Users

> **Summary:** Verify that an admin can filter users in the Users page using the various filter options.

**Preconditions:**

- User must be an admin and using a desktop/PC.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                      |
| --- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                                  |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.                   |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.          |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.       |
| 5   | In the sidebar, navigate to the `Users` page.                                              | Verify that the Users page is displayed with the user table.           |
| 6   | Locate the filter buttons above the user table.                                            | Verify that filter options are visible and available.                  |
| 7   | Click on a specific filter button (e.g., Active Users).                                    | Verify that the table updates to show only the filtered results.       |
| 8   | Click on a different filter button (e.g., Archived Users).                                 | Verify that the table updates to show only the newly filtered results. |
| 9   | Click on the "All Users" button (if available).                                            | Verify that all users are displayed in the table again.                |

**Post-conditions:**

- The user table accurately displays users based on the selected filters.
- The admin can easily switch between different filter views.
