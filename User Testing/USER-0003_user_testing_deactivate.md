## **USER-0004:** User testing - Deactivate User Account

> **Summary:** Verify that an admin can deactivate a user account from the Users page using the desktop interface.

**Preconditions:**

- User must be an admin and using a desktop/PC.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                |
| --- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                            |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.             |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.    |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately. |
| 5   | In the sidebar, navigate to the `Users` page.                                              | Verify that the Users page is displayed.                         |
| 6   | Select a user from the table, click the `Actions` button, then click `Disable Account`.    | Verify that a confirmation dialog appears.                       |
| 7   | Click the `OK` button in the confirmation dialog.                                          | Verify that the selected user's account is deactivated.          |

**Post-conditions:**

- The selected user's account is deactivated and reflected in the user list.
