<!-- filepath: c:\projects\KyutoTCM\Settings Testing\Organization Information\SET-0006_organization_information_change_logo_testing.md -->

## **SET-0006:** Organization Information testing - Change Logo

> **Summary:** Verify that organizations can change their logo by clicking on their current logo and uploading a new image.

**Preconditions:**

- User must be logged in as an organization.
- Organization must have existing profile information and logo.

Scenario 1: Change Organization Logo with Valid Image

| #   | Step                                                                        | Expected Behavior                                                                                             |
| --- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                         | Verify that the home screen is shown.                                                                         |
| 2   | For desktop, click the `Organization` link in the sidebar.                  | Verify that the Organization page is displayed.                                                               |
| 3   | For mobile, tap the burger icon and select `Organization` from the sidebar. | Verify that the Organization page is displayed.                                                               |
| 4   | Locate the organization's current logo on the Organization page.            | Verify that the current logo is displayed.                                                                    |
| 5   | Hover over the logo image.                                                  | Verify that a hover effect or edit indicator appears (e.g., camera icon, pencil icon, or "Change logo" text). |
| 6   | Click on the logo image.                                                    | Verify that an upload dialog or file picker opens.                                                            |
| 7   | Select a valid image file (e.g., JPG, PNG) from your local system.          | Verify that the file is accepted and selected for upload.                                                     |
| 8   | Click the "Upload", "Save", or "Confirm" button.                            | Verify that a loading indicator appears during the upload process.                                            |
| 9   | Wait for the upload process to complete.                                    | Verify that a success message appears.                                                                        |
| 10  | Observe the displayed logo after the upload completes.                      | Verify that the new logo is immediately displayed without a page refresh.                                     |
| 11  | Refresh the Organization page.                                              | Verify that the new logo persists after the page refresh.                                                     |
| 12  | Navigate to other parts of the application where the logo is displayed.     | Verify that the logo is updated consistently throughout the application.                                      |

Scenario 2: Image Validation and Error Handling

| #   | Step                                                                                       | Expected Behavior                                                                |
| --- | ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------- |
| 1   | Navigate to the Organization page and click on the logo as in steps 1-6 from Scenario 1.   | Verify that the upload dialog or file picker opens.                              |
| 2   | Attempt to select a file with an unsupported format (e.g., .exe, .pdf, .doc).              | Verify that an error message appears indicating valid file formats.              |
| 3   | Attempt to select an image file larger than 10 MB.                                         | Verify that an error message appears indicating the 10 MB file size restriction. |
| 4   | Attempt to select an image with very small dimensions (e.g., 10x10 pixels).                | Verify that an error message appears indicating minimum image dimensions.        |
| 5   | Cancel the upload dialog.                                                                  | Verify that no changes are made to the logo and the dialog closes.               |
| 6   | Click the logo again and select a valid image just under 10 MB.                            | Verify that the file is accepted for upload.                                     |
| 7   | Simulate a network error during upload (e.g., disconnect network temporarily if possible). | Verify that an appropriate error message appears.                                |
| 8   | Reconnect network and try again with a valid image.                                        | Verify that the upload completes successfully.                                   |

Scenario 3: Logo Preview and Cropping

| #   | Step                                                                                     | Expected Behavior                                                       |
| --- | ---------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| 1   | Navigate to the Organization page and click on the logo as in steps 1-6 from Scenario 1. | Verify that the upload dialog or file picker opens.                     |
| 2   | Select a valid image file that is not square.                                            | Verify that a preview/cropping tool appears showing the selected image. |
| 3   | Use the cropping tool to adjust the visible portion of the image.                        | Verify that the crop area can be adjusted and moved.                    |
| 4   | Zoom in or out on the image if such controls are available.                              | Verify that the zoom controls function correctly.                       |
| 5   | Click the "Apply" or "Save" button after cropping.                                       | Verify that the cropping is applied and the upload process begins.      |
| 6   | Wait for the upload process to complete.                                                 | Verify that a success message appears.                                  |
| 7   | Observe the displayed logo after the upload completes.                                   | Verify that the new logo is displayed with the applied cropping.        |

**Post-conditions:**

- The organization's logo is updated in the system.
- The new logo is immediately visible in the Organization page without requiring a refresh.
- The new logo is consistently displayed across all areas of the application where the organization's logo appears.
- Image validation correctly enforces the 10 MB file size restriction and acceptable file formats.
- The logo upload process provides appropriate feedback during all stages, including selection, preview, upload, and completion.
