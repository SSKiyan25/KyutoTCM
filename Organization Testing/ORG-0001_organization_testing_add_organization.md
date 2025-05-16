## **ORG-0001:** Organization testing - Add Organization

> **Summary:** Verify that an admin can create a new organization and that the verification process works correctly.

**Preconditions:**

- User must be an admin and using a desktop/PC.
- Admin must have access to a valid Gmail account for verification.

Scenario 1

| #   | Step                                                                                       | Expected Behavior                                                |
| --- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------- |
| 1   | Launch application.                                                                        | Verify that the home screen is shown.                            |
| 2   | Go to the login page, scroll to the bottom, and click `Login as admin`.                    | Verify that the admin login modal/page is displayed.             |
| 3   | Enter the correct admin pin: `5878`.                                                       | Verify that the pin is accepted and admin login form appears.    |
| 4   | Log in with admin credentials: email: cscubeverch_admin@gmail.com, password: V3erch_cs3b4. | Verify that the admin is logged in and redirected appropriately. |
| 5   | In the sidebar, navigate to the `Organizations` page.                                      | Verify that the Organizations page is displayed.                 |
| 6   | Locate and click the `Add Organization` card/button.                                       | Verify that the Add Organization modal appears.                  |
| 7   | Enter a valid organization name in the Name field.                                         | Verify that the name is accepted.                                |
| 8   | Enter a valid Gmail address in the Email field.                                            | Verify that the email is accepted.                               |
| 9   | Enter a valid password in the Password field.                                              | Verify that the password is accepted.                            |
| 10  | Click the `Create` button.                                                                 | Verify that a success message appears and modal closes.          |
| 11  | Access the Gmail account used for the organization.                                        | Verify that a verification email was received.                   |
| 12  | Open the verification email and click the verification link.                               | Verify that the link opens and verification is successful.       |

**Post-conditions:**

- A new organization is created in the system.
- The organization's email is verified.
- The organization appears in the organizations list.
