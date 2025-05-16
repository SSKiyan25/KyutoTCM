## **ORG-0005:** Organization testing - Search Organizations

> **Summary:** Verify that an admin can search for organizations using the search bar above the organizations table.

**Preconditions:**

- User must be an admin and using a desktop/PC.
- Multiple organizations must exist in the system.

Scenario 1

| #   | Step                                                                                                 | Expected Behavior                                                                  |
| --- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                  | Verify that the home screen is shown.                                              |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                              | Verify that the admin login modal/page is displayed.                               |
| 3   | Enter the correct admin pin: `5878`.                                                                 | Verify that the pin is accepted and admin login form appears.                      |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4.           | Verify that the admin is logged in and redirected appropriately.                   |
| 5   | In the sidebar, navigate to the `Organizations` page.                                                | Verify that the Organizations page is displayed with a table of organizations.     |
| 6   | Locate the search bar above the organizations table.                                                 | Verify that the search bar is visible and clickable.                               |
| 7   | Enter a known organization name in the search bar.                                                   | Verify that the input is accepted.                                                 |
| 8   | Press Enter or click the search button.                                                              | Verify that the table updates to show only organizations matching the search term. |
| 9   | Clear the search bar and enter a partial organization name that should match multiple organizations. | Verify that all matching organizations are displayed in the table.                 |
| 10  | Enter a search term that doesn't match any organization.                                             | Verify that the table shows no results or an appropriate message.                  |
| 11  | Clear the search bar completely.                                                                     | Verify that all organizations are displayed again in the table.                    |

**Post-conditions:**

- The organizations table correctly filters organizations based on the search terms.
- The admin can efficiently find specific organizations using the search feature.
