## **ORG-0007:** Organization testing - Archive Organization

> **Summary:** Verify that an admin can archive an organization using the actions button.

**Preconditions:**

- User must be an admin and using a desktop/PC.
- At least one active organization must exist in the system.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                              |
| --- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                                          |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.                           |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.                  |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.               |
| 5   | In the sidebar, navigate to the `Organizations` page.                                      | Verify that the Organizations page is displayed with a table of organizations. |
| 6   | Locate an active organization in the table.                                                | Verify that the organization entry is displayed with an actions button.        |
| 7   | Click on the actions button for the selected organization.                                 | Verify that a dropdown menu of actions appears.                                |
| 8   | Click on the `Archive` option in the dropdown menu.                                        | Verify that a confirmation dialog appears.                                     |
| 9   | Click `OK` or `Confirm` in the confirmation dialog.                                        | Verify that the dialog closes and a success message appears.                   |
| 10  | Check the status of the organization in the table.                                         | Verify that the organization is now marked as "Archived".                      |
| 11  | (Optional) Apply the "Archived" filter to the table.                                       | Verify that the newly archived organization appears in the filtered results.   |

**Post-conditions:**

- The selected organization is successfully archived.
- The organization's status is updated to "Archived" in the system.
- The archived organization appears when filtering for archived organizations.
