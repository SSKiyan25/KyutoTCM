<!-- filepath: c:\projects\KyutoTCM\Settings Testing\Organization Information\SET-0007_organization_information_change_name_testing.md -->

## **SET-0007:** Organization Information testing - Change Name

> **Summary:** Verify that organizations can change their name and the change is properly reflected throughout the system, including product references and store URLs.

**Preconditions:**

- User must be logged in as an organization.
- Organization must have existing profile information.
- Organization must have at least one product listed.

Scenario 1: Change Organization Name with Valid Input

| #   | Step                                                                        | Expected Behavior                                                        |
| --- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| 1   | Launch application.                                                         | Verify that the home screen is shown.                                    |
| 2   | For desktop, click the `Organization` link in the sidebar.                  | Verify that the Organization page is displayed.                          |
| 3   | For mobile, tap the burger icon and select `Organization` from the sidebar. | Verify that the Organization page is displayed.                          |
| 4   | Locate the organization name field or section.                              | Verify that the current organization name is displayed.                  |
| 5   | Click the "Edit" or pencil icon button next to the organization name.       | Verify that the organization name field becomes editable.                |
| 6   | Edit the organization name with a new valid name.                           | Verify that the input is accepted.                                       |
| 7   | Click the "Save" or "Apply Changes" button.                                 | Verify that a loading indicator appears.                                 |
| 8   | Wait for the save operation to complete.                                    | Verify that a success message appears.                                   |
| 9   | Observe the displayed organization name after saving.                       | Verify that the updated name is immediately displayed without a refresh. |
| 10  | Refresh the Organization page.                                              | Verify that the new name persists after the page refresh.                |

Scenario 2: Verify Organization Name Change Reflected in Products

| #   | Step                                                                                 | Expected Behavior                                                             |
| --- | ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------- |
| 1   | After changing the organization name, navigate to the Products page.                 | Verify that the Products page loads successfully.                             |
| 2   | Locate a product that belongs to the organization.                                   | Verify that the product lists the updated organization name.                  |
| 3   | Click on the product to view its details.                                            | Verify that the product detail page opens.                                    |
| 4   | Check the organization name displayed on the product detail page.                    | Verify that the updated organization name is shown.                           |
| 5   | Navigate to the storefront or product listing visible to customers.                  | Verify that products show the updated organization name in the storefront.    |
| 6   | Check any filtering or sorting options by organization.                              | Verify that the updated organization name appears in filters/sorting options. |
| 7   | If there are organization-specific sections or collections, navigate to those areas. | Verify that these areas display the updated organization name.                |

Scenario 3: Verify Organization Name Change Reflected in Store URL

| #   | Step                                                                           | Expected Behavior                                                                     |
| --- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| 1   | After changing the organization name, open a new browser tab.                  | Verify that a new tab opens.                                                          |
| 2   | Navigate to the store URL using the original format: `/stores/[old-org-name]`. | Verify the behavior: either redirect to new URL or show appropriate message.          |
| 3   | Navigate to the store URL using the updated format: `/stores/[new-org-name]`.  | Verify that the organization's store page loads successfully.                         |
| 4   | Check all content and branding on the store page.                              | Verify that all instances of the organization name are updated.                       |
| 5   | Check navigation breadcrumbs if available.                                     | Verify that breadcrumbs show the correct updated organization name.                   |
| 6   | Check page title and meta tags if possible.                                    | Verify that metadata contains the updated organization name.                          |
| 7   | Perform a search for the organization using the new name.                      | Verify that search results find the organization with its updated name.               |
| 8   | Perform a search for the organization using the old name.                      | Verify whether the system still associates the old name with the organization or not. |

Scenario 4: Input Validation for Organization Name

| #   | Step                                                                         | Expected Behavior                                                             |
| --- | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| 1   | Navigate to the organization name edit form as in steps 1-5 from Scenario 1. | Verify that the organization name field becomes editable.                     |
| 2   | Attempt to save an empty organization name.                                  | Verify that an error message appears indicating name is required.             |
| 3   | Attempt to enter a very short name (e.g., 1-2 characters).                   | Verify that an error message appears indicating minimum length requirement.   |
| 4   | Attempt to enter a very long name (exceeding maximum character limit).       | Verify that the input is truncated or an error message appears.               |
| 5   | Attempt to enter special characters that might not be allowed.               | Verify that invalid characters are either prevented or flagged with an error. |
| 6   | Attempt to enter a name that already belongs to another organization.        | Verify that an error message appears indicating the name is already taken.    |
| 7   | Enter a valid organization name.                                             | Verify that the input is accepted without errors.                             |
| 8   | Click the "Save" or "Apply Changes" button.                                  | Verify that the changes are saved successfully.                               |

**Post-conditions:**

- The organization name is updated in the system.
- The updated name is immediately visible in the Organization page without requiring a refresh.
- The updated name is reflected in all products owned by the organization.
- The store URL is updated to reflect the new organization name.
- All references to the organization across the system show the updated name.
- The system properly handles navigation attempts using the old organization name/URL.
