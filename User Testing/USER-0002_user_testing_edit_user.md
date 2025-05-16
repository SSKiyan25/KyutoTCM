## **USER-0003:** User testing - Edit User Information

> **Summary:** Verify that a logged-in user can edit their profile information and changes are reflected immediately after saving.

**Preconditions:**

- User must be logged in.

Scenario 1

| #   | Step                                                                                  | Expected Behavior                                            |
| --- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| 1   | Launch application.                                                                   | Verify that the home screen is shown.                        |
| 2   | In the navbar dropdown (desktop), click the `Profile` link.                           | Verify that the profile page is displayed.                   |
| 3   | On mobile, open the sidebar via the burger icon and tap the `Profile` link.           | Verify that the profile page is displayed.                   |
| 4   | In the profile page, click the `Edit` button for a section (e.g., Name, Email, etc.). | Verify that the edit modal for the selected section appears. |
| 5   | Modify the desired field(s) in the modal.                                             | Verify that input fields are validated using regex.          |
| 6   | Click the `Save` button.                                                              | Verify that the modal closes and the profile page updates.   |
| 7   | Check the updated information on the profile page.                                    | Verify that the changes are reflected immediately.           |

**Post-conditions:**

- The user's updated information is saved and displayed on their profile page.
