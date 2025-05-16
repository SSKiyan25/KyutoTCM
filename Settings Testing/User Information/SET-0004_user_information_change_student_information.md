## **SET-0004:** User Information testing - Change Student Information

> **Summary:** Verify that users can edit their student information in the profile page and that input validation using regex patterns works correctly.

**Preconditions:**

- User must be logged in with a student account.
- User must have existing student information.

Scenario 1: Edit Student Information with Valid Data

| #   | Step                                                                    | Expected Behavior                                                               |
| --- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| 1   | Launch application.                                                     | Verify that the home screen is shown.                                           |
| 2   | Click on the user profile icon or name in the navigation bar/header.    | Verify that the user profile dropdown menu appears.                             |
| 3   | Select "Profile" or "Settings" from the dropdown menu.                  | Verify that the profile page loads successfully.                                |
| 4   | Navigate to the "Student Information" section of the profile page.      | Verify that the current student information is displayed correctly.             |
| 5   | Click the "Edit" or pencil icon button next to the student information. | Verify that the student information fields become editable.                     |
| 6   | Edit the Student ID field with a valid format (e.g., "20-1-01709").     | Verify that the input is accepted.                                              |
| 7   | Edit the Course field with a valid format (e.g., "BSCS").               | Verify that the input is accepted.                                              |
| 8   | Edit the College field with a valid format (e.g., "FOC").               | Verify that the input is accepted.                                              |
| 9   | Click the "Save" or "Apply Changes" button.                             | Verify that a loading indicator appears.                                        |
| 10  | Wait for the save operation to complete.                                | Verify that a success message appears.                                          |
| 11  | Observe the displayed student information after saving.                 | Verify that the updated information is immediately displayed without a refresh. |

Scenario 2: Input Validation with Regex Patterns

| #   | Step                                                                              | Expected Behavior                                                                |
| --- | --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| 1   | Navigate to the student information edit form as in steps 1-5 from Scenario 1.    | Verify that the student information fields become editable.                      |
| 2   | Attempt to enter an invalid Student ID format (e.g., "ABC123" or "20101709").     | Verify that an error message appears indicating the correct format (XX-X-XXXXX). |
| 3   | Enter a valid Student ID format (e.g., "20-1-01709").                             | Verify that the input is accepted without errors.                                |
| 4   | Attempt to leave the Course field empty.                                          | Verify that an error message appears indicating this is a required field.        |
| 5   | Enter a valid Course (e.g., "BSCS" or "Bachelor of Science in Computer Science"). | Verify that the input is accepted without errors.                                |
| 6   | Attempt to leave the College field empty.                                         | Verify that an error message appears indicating this is a required field.        |
| 7   | Enter a valid College (e.g., "FOC" or "Faculty of Computing").                    | Verify that the input is accepted without errors.                                |
| 8   | Click the "Save" or "Apply Changes" button.                                       | Verify that the changes are saved successfully.                                  |

Scenario 3: Verify Form Behavior and Real-time Feedback

| #   | Step                                                                                                                  | Expected Behavior                                                                      |
| --- | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| 1   | Navigate to the student information edit form as in steps 1-5 from Scenario 1.                                        | Verify that the student information fields become editable.                            |
| 2   | Begin typing an invalid Student ID format.                                                                            | Verify that real-time validation feedback appears as you type.                         |
| 3   | Enter an invalid Student ID and then move to the next field.                                                          | Verify that an error message appears immediately after focusing away from the field.   |
| 4   | Correct the Student ID to match the required format (XX-X-XXXXX).                                                     | Verify that the error message disappears once the input becomes valid.                 |
| 5   | Enter abbreviations for Course (e.g., "BSCS") and College (e.g., "FOC").                                              | Verify that abbreviations are accepted as valid inputs.                                |
| 6   | Enter full names for Course and College (e.g., "Bachelor of Science in Computer Science" and "Faculty of Computing"). | Verify that full names are also accepted as valid inputs.                              |
| 7   | Click "Cancel" or a similar button if available.                                                                      | Verify that any changes are discarded and the original information is still displayed. |
| 8   | Re-open the edit form and make valid changes.                                                                         | Verify that the form accepts the valid changes.                                        |
| 9   | Click the "Save" or "Apply Changes" button.                                                                           | Verify that the changes are saved and reflected immediately in the profile display.    |
| 10  | Refresh the page.                                                                                                     | Verify that the changes persist after a page refresh.                                  |

**Post-conditions:**

- User student information is updated in the system.
- Updated information is immediately visible in the profile page without requiring a refresh.
- Input validation successfully prevents invalid data from being submitted.
- Student ID is properly validated against the required format (XX-X-XXXXX).
- Course and College fields accept both abbreviations (BSCS, FOC) and full names.
- Form provides appropriate visual feedback for both valid and invalid inputs.
