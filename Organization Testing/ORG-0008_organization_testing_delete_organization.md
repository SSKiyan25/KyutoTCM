## **ORG-0008:** Organization testing - Delete Organization

> **Summary:** Verify that an admin can delete an organization using the actions button.

**Preconditions:**

- User must be an admin and using a desktop/PC.
- At least one organization must exist in the system.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                              |
| --- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                                          |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.                           |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.                  |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately.               |
| 5   | In the sidebar, navigate to the `Organizations` page.                                      | Verify that the Organizations page is displayed with a table of organizations. |
| 6   | Locate the organization to be deleted in the table.                                        | Verify that the organization entry is displayed with an actions button.        |
| 7   | Click on the actions button for the selected organization.                                 | Verify that a dropdown menu of actions appears.                                |
| 8   | Click on the `Delete` option in the dropdown menu.                                         | Verify that a confirmation dialog appears.                                     |
| 9   | Click `OK` or `Confirm` in the confirmation dialog.                                        | Verify that the dialog closes and a success message appears.                   |
| 10  | Check the organizations table.                                                             | Verify that the deleted organization no longer appears in the table.           |

**Post-conditions:**

- The selected organization is permanently deleted from the system.
- The organization no longer appears in any filters or search results.
- Any associated data is handled according to the system's data retention policies.
