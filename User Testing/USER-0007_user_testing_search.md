## **USER-0008:** User testing - Search Users

> **Summary:** Verify that an admin can search for specific users using the search bar in the Users page.

**Preconditions:**

- User must be an admin and using a desktop/PC.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                     |
| --- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                                 |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.                  |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.         |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.      |
| 5   | In the sidebar, navigate to the `Users` page.                                              | Verify that the Users page is displayed with the user table.          |
| 6   | Locate the search bar above the user table.                                                | Verify that the search bar is visible and available.                  |
| 7   | Enter a known email in the search bar (e.g., "john.doe@example.com").                      | Verify that the search input is                                       |
| 8   | Clear the search bar and enter a partial name or email that should match multiple users.   | Verify that all users matching the partial search term are displayed. |
| 10  | Clear the search bar completely.                                                           | Verify that the full list of users is restored.                       |

**Post-conditions:**

- The user table accurately displays search results based on the entered search terms.
- The search feature helps admins quickly find specific users in the system.
