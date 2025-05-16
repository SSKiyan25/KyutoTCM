## **ORG-0004:** Organization testing - Filter Organizations by Status

> **Summary:** Verify that an admin can filter organizations in the table by their status using the dropdown menu.

**Preconditions:**

- User must be an admin and using a desktop/PC.
- Multiple organizations with different statuses must exist in the system.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                                        |
| --- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                                                    |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.                                     |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.                            |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.                         |
| 5   | In the sidebar, navigate to the `Organizations` page.                                      | Verify that the Organizations page is displayed with a table of organizations.           |
| 6   | Locate the status filter dropdown menu above the organizations table.                      | Verify that the dropdown menu is visible and clickable.                                  |
| 7   | Click on the dropdown menu to open it.                                                     | Verify that the dropdown shows all available status options.                             |
| 8   | Select a specific status (e.g., "Active").                                                 | Verify that the table updates to show only organizations with that status.               |
| 9   | Select a different status from the dropdown menu.                                          | Verify that the table updates to show only organizations with the newly selected status. |
| 10  | Select "All" or similar option to reset the filter.                                        | Verify that the table displays all organizations again.                                  |

**Post-conditions:**

- The organizations table correctly filters organizations by the selected status.
- The filter dropdown accurately indicates which filter is currently applied.
- Admin understands the relationship between organization status and commission rates.
