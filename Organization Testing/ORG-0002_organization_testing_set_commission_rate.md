## **ORG-0002:** Organization testing - Set Commission Rate

> **Summary:** Verify that an admin can set a new commission rate for organizations.

**Preconditions:**

- User must be an admin and using a desktop/PC.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                |
| --- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                            |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.             |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.    |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately. |
| 5   | In the sidebar, navigate to the `Organizations` page.                                      | Verify that the Organizations page is displayed.                 |
| 6   | Locate the commission rate card which displays the current rate.                           | Verify that the current commission rate is visible.              |
| 7   | Click the button on the commission rate card to change the rate.                           | Verify that the Set Commission Rate modal appears.               |
| 8   | Enter a new percentage value in the rate field (e.g., "15").                               | Verify that the new rate value is accepted.                      |
| 9   | (Optional) Enter remarks in the remarks field explaining the reason for the change.        | Verify that the remarks are accepted.                            |
| 10  | Click the `Save` or `Update` button.                                                       | Verify that a success message appears and modal closes.          |
| 11  | Check the commission rate card on the Organizations page.                                  | Verify that it now displays the updated commission rate.         |

**Post-conditions:**

- The commission rate is updated to the new value.
- The commission rate change is logged with the optional remarks.
- All relevant calculations in the system now use the new commission rate.
