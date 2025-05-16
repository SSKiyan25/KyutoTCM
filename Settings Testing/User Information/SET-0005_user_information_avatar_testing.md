## **SET-0005:** User Information testing - Change Avatar

> **Summary:** Verify that users can change their profile avatar by clicking on their current avatar and uploading a new image.

**Preconditions:**

- User must be logged in with a standard user account.
- User must have existing profile information and avatar.

Scenario 1: Change Avatar with Valid Image

| #   | Step                                                                      | Expected Behavior                                                                                                |
| --- | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                       | Verify that the home screen is shown.                                                                            |
| 2   | Click on the user profile icon or name in the navigation bar/header.      | Verify that the user profile dropdown menu appears.                                                              |
| 3   | Select "Profile" or "Settings" from the dropdown menu.                    | Verify that the profile page loads successfully.                                                                 |
| 4   | Locate the user's current avatar/profile picture on the profile page.     | Verify that the current avatar is displayed.                                                                     |
| 5   | Hover over the avatar image.                                              | Verify that a hover effect or edit indicator appears (e.g., camera icon, pencil icon, or "Change picture" text). |
| 6   | Click on the avatar image.                                                | Verify that an upload dialog or file picker opens.                                                               |
| 7   | Select a valid image file (e.g., JPG, PNG) from your local system.        | Verify that the file is accepted and selected for upload.                                                        |
| 8   | Click the "Upload", "Save", or "Confirm" button.                          | Verify that a loading indicator appears during the upload process.                                               |
| 9   | Wait for the upload process to complete.                                  | Verify that a success message appears.                                                                           |
| 10  | Observe the displayed avatar after the upload completes.                  | Verify that the new avatar is immediately displayed without a page refresh.                                      |
| 11  | Refresh the profile page.                                                 | Verify that the new avatar persists after the page refresh.                                                      |
| 12  | Navigate to other parts of the application where the avatar is displayed. | Verify that the avatar is updated consistently throughout the application.                                       |

Scenario 2: Image Validation and Error Handling

| #   | Step                                                                                       | Expected Behavior                                                                  |
| --- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------- |
| 1   | Navigate to the profile page and click on the avatar as in steps 1-6 from Scenario 1.      | Verify that the upload dialog or file picker opens.                                |
| 2   | Attempt to select a file with an unsupported format (e.g., .exe, .pdf, .doc).              | Verify that an error message appears indicating valid file formats.                |
| 3   | Attempt to select a very large image file (e.g., >5MB).                                    | Verify that an error message appears indicating the maximum file size.             |
| 4   | Attempt to select an image with very small dimensions (e.g., 10x10 pixels).                | Verify that an error message appears indicating minimum image dimensions.          |
| 5   | Attempt to select an image with very large dimensions (e.g., 5000x5000 pixels).            | Verify that either the image is automatically resized or an error message appears. |
| 6   | Cancel the upload dialog.                                                                  | Verify that no changes are made to the avatar and the dialog closes.               |
| 7   | Click the avatar again and select a valid image.                                           | Verify that the file is accepted for upload.                                       |
| 8   | Simulate a network error during upload (e.g., disconnect network temporarily if possible). | Verify that an appropriate error message appears.                                  |
| 9   | Reconnect network and try again with a valid image.                                        | Verify that the upload completes successfully.                                     |

Scenario 3: Avatar Preview and Cropping

| #   | Step                                                                                  | Expected Behavior                                                       |
| --- | ------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| 1   | Navigate to the profile page and click on the avatar as in steps 1-6 from Scenario 1. | Verify that the upload dialog or file picker opens.                     |
| 2   | Select a valid image file that is not square.                                         | Verify that a preview/cropping tool appears showing the selected image. |
| 3   | Use the cropping tool to adjust the visible portion of the image.                     | Verify that the crop area can be adjusted and moved.                    |
| 4   | Zoom in or out on the image if such controls are available.                           | Verify that the zoom controls function correctly.                       |
| 5   | Click the "Apply" or "Save" button after cropping.                                    | Verify that the cropping is applied and the upload process begins.      |
| 6   | Wait for the upload process to complete.                                              | Verify that a success message appears.                                  |
| 7   | Observe the displayed avatar after the upload completes.                              | Verify that the new avatar is displayed with the applied cropping.      |

**Post-conditions:**

- The user's avatar is updated in the system.
- The new avatar is immediately visible in the profile page without requiring a refresh.
- The new avatar is consistently displayed across all areas of the application where the user's avatar appears.
- Image validation correctly enforces acceptable file formats, dimensions, and sizes.
- The avatar upload process provides appropriate feedback during all stages, including selection, preview, upload, and completion.
