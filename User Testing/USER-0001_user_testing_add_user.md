## **USER-0002:** User testing - Add User via Google Login

> **Summary:** Verify that a user is added automatically to the database after logging in through the Google button on the login page.

**Preconditions:**

- No user is currently logged in.

Scenario 1

| #   | Step                                                            | Expected Behavior                                             |
| --- | --------------------------------------------------------------- | ------------------------------------------------------------- |
| 1   | Launch application.                                             | Verify that the home screen is shown.                         |
| 2   | On desktop, locate and click the `Login` link in the navbar.    | Verify that the login page is displayed.                      |
| 3   | On mobile, open the footer or sidebar and tap the `Login` link. | Verify that the login page is displayed.                      |
| 4   | On the login page, click the `Login with Google` button.        | Verify that the Google authentication popup appears.          |
| 5   | Complete the Google login process.                              | Verify that the user is redirected to the home or users page. |
| 6   | Check the database or user list.                                | Verify that the new user is added automatically.              |

**Post-conditions:**

- The user is added to the database and is now logged in.
