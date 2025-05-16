## **SET-0003:** User Information testing - Change Personal Information

> **Summary:** Verify that users can edit their personal information in the profile page and that input validation using regex patterns works correctly.

**Preconditions:**

- User must be logged in with a standard user account.
- User must have existing profile information.

Scenario 1: Edit Personal Information with Valid Data

| #   | Step                                                                     | Expected Behavior                                                               |
| --- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------------- |
| 1   | Launch application.                                                      | Verify that the home screen is shown.                                           |
| 2   | Click on the user profile icon or name in the navigation bar/header.     | Verify that the user profile dropdown menu appears.                             |
| 3   | Select "Profile" or "Settings" from the dropdown menu.                   | Verify that the profile page loads successfully.                                |
| 4   | Navigate to the "Personal Information" section of the profile page.      | Verify that the current personal information is displayed correctly.            |
| 5   | Click the "Edit" or pencil icon button next to the personal information. | Verify that the personal information fields become editable.                    |
| 6   | Edit the First Name field with valid characters (letters only).          | Verify that the input is accepted.                                              |
| 7   | Edit the Last Name field with valid characters (letters only).           | Verify that the input is accepted.                                              |
| 8   | Edit the Email Address field with a valid email format.                  | Verify that the input is accepted.                                              |
| 9   | Edit the Phone Number field with a valid format (e.g., "+639123456789"). | Verify that the input is accepted.                                              |
| 10  | Edit the Username field with a valid username format.                    | Verify that the input is accepted.                                              |
| 11  | Click the "Save" or "Apply Changes" button.                              | Verify that a loading indicator appears.                                        |
| 12  | Wait for the save operation to complete.                                 | Verify that a success message appears.                                          |
| 13  | Observe the displayed personal information after saving.                 | Verify that the updated information is immediately displayed without a refresh. |

Scenario 2: Input Validation with Regex Patterns

| #   | Step                                                                                   | Expected Behavior                                                                |
| --- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| 1   | Navigate to the personal information edit form as in steps 1-5 from Scenario 1.        | Verify that the personal information fields become editable.                     |
| 2   | Attempt to enter numbers or special characters in the First Name field.                | Verify that the input is either rejected or an error message appears.            |
| 3   | Attempt to enter numbers or special characters in the Last Name field.                 | Verify that the input is either rejected or an error message appears.            |
| 4   | Attempt to enter an invalid email address format (e.g., "user@" or "user.com").        | Verify that an error message appears indicating the correct email format.        |
| 5   | Attempt to enter an invalid phone number format (e.g., "abcdefg" or "12345").          | Verify that an error message appears indicating the correct phone number format. |
| 6   | Attempt to enter a username with invalid characters or too short (less than 3 chars).  | Verify that an error message appears indicating the username requirements.       |
| 7   | Enter an extremely long string in any text field (exceeding maximum character limits). | Verify that the input is truncated or an error message appears.                  |
| 8   | Leave a required field empty (if any fields are required).                             | Verify that an error message appears and form submission is prevented.           |
| 9   | Enter valid inputs for all fields.                                                     | Verify that no error messages appear.                                            |
| 10  | Click the "Save" or "Apply Changes" button.                                            | Verify that the changes are saved successfully.                                  |

Scenario 3: Verify Form Behavior and Real-time Feedback

| #   | Step                                                                             | Expected Behavior                                                                      |
| --- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| 1   | Navigate to the personal information edit form as in steps 1-5 from Scenario 1.  | Verify that the personal information fields become editable.                           |
| 2   | Begin typing in a field with regex validation (e.g., Phone Number).              | Verify that real-time validation feedback appears as you type.                         |
| 3   | Enter an invalid value and then move to the next field (blur the current field). | Verify that an error message appears immediately after focusing away from the field.   |
| 4   | Correct the invalid value to meet the regex requirements.                        | Verify that the error message disappears once the input becomes valid.                 |
| 5   | Click "Cancel" or a similar button if available.                                 | Verify that any changes are discarded and the original information is still displayed. |
| 6   | Re-open the edit form and make valid changes.                                    | Verify that the form accepts the valid changes.                                        |
| 7   | Click the "Save" or "Apply Changes" button.                                      | Verify that the changes are saved and reflected immediately in the profile display.    |
| 8   | Refresh the page.                                                                | Verify that the changes persist after a page refresh.                                  |

**Post-conditions:**

- User personal information is updated in the system.
- Updated information is immediately visible in the profile page without requiring a refresh.
- Input validation successfully prevents invalid data from being submitted.
- Regex patterns properly validate:
  - First name and last name (letters only)
  - Email address (valid email format)
  - Phone number (specific format)
  - Username (valid characters and length requirements)
- Form provides appropriate visual feedback for both valid and invalid inputs.
