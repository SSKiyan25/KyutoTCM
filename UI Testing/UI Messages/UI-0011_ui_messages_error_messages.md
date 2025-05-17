<!-- filepath: c:\projects\KyutoTCM\UI Testing\UI Messages\UI-0011_ui_messages_error_messages.md -->

## **UI-0011:** UI Messages Testing - Error Messages Display

> **Summary:** Verify that error messages in various parts of the application are displayed correctly, follow consistent styling guidelines, and provide clear information according to the design guidelines in https://github.com/SSKiyan25/kyuto.

**Preconditions:**

- Tester has access to the Verch application
- Tester has appropriate permissions to access all application sections

### 1. Form Field Error Message Display

| #   | Display Type            | Test Description                            | Expected Behavior                                             |
| --- | ----------------------- | ------------------------------------------- | ------------------------------------------------------------- |
| 1.1 | Inline Field Errors     | Verify error styling below input fields     | Error text appears with proper color, icon, and spacing       |
| 1.2 | Required Field Markers  | Check required field error indicators       | Required field errors highlight with consistent styling       |
| 1.3 | Field Highlighting      | Test input field border/background on error | Field visually indicates error state with color/border        |
| 1.4 | Error Icon Display      | Verify error icon placement and styling     | Error icons display consistently across different field types |
| 1.5 | Character Limit Display | Check character limit error visualization   | Over-limit indicators display with proper styling             |

### 2. Form-Level Error Message Display

| #   | Display Type           | Test Description                          | Expected Behavior                                            |
| --- | ---------------------- | ----------------------------------------- | ------------------------------------------------------------ |
| 2.1 | Error Summary Banner   | Check form error summary banner display   | Error summary appears at form top with proper styling        |
| 2.2 | Form Section Errors    | Verify section-specific error display     | Section with errors indicates issues with consistent styling |
| 2.3 | Multiple Error Display | Test display when multiple errors present | Multiple errors stack/group according to design guidelines   |
| 2.4 | Form Submission Errors | Check styling of post-submission errors   | Submission errors display prominently with clear styling     |
| 2.5 | Error Navigation Links | Verify error summary navigation links     | Error links navigate focus to corresponding fields           |

### 3. Modal & Dialog Error Message Display

| #   | Display Type            | Test Description                           | Expected Behavior                                            |
| --- | ----------------------- | ------------------------------------------ | ------------------------------------------------------------ |
| 3.1 | Modal Error Banners     | Check error banner in modal dialogs        | Error banners display at top of modal with proper styling    |
| 3.2 | Dialog Warning Display  | Verify warning dialog styling and layout   | Warning dialogs use consistent color/icon conventions        |
| 3.3 | Confirmation Errors     | Test error display in confirmation dialogs | Errors in confirmation flows follow styling guidelines       |
| 3.4 | Modal Form Field Errors | Check field error display within modals    | Modal field errors match styling of main form field errors   |
| 3.5 | Action Button Errors    | Verify error state on modal action buttons | Error states on buttons follow consistent styling guidelines |

### 4. Page-Level Error Message Display

| #   | Display Type           | Test Description                       | Expected Behavior                                           |
| --- | ---------------------- | -------------------------------------- | ----------------------------------------------------------- |
| 4.1 | Page Error Banners     | Check page-level error banner display  | Page errors display at top of content with proper styling   |
| 4.2 | Full Page Error States | Verify full-page error display         | Full page errors display with consistent layout and styling |
| 4.3 | Error Page Navigation  | Test navigation options on error pages | Error pages provide clear navigation/retry options          |
| 4.4 | HTTP Error Pages       | Check custom HTTP error page styling   | HTTP error pages follow application styling guidelines      |
| 4.5 | Status Code Display    | Verify error code display conventions  | Error codes display consistently when applicable            |

### 5. Error Message Accessibility

| #   | Feature                | Test Description                           | Expected Behavior                                       |
| --- | ---------------------- | ------------------------------------------ | ------------------------------------------------------- |
| 5.1 | Screen Reader Support  | Check error announcement to screen readers | Errors are properly announced by screen readers         |
| 5.2 | Error Focus Management | Verify keyboard focus moves to errors      | Focus moves to errors or error summary appropriately    |
| 5.3 | Color Contrast         | Test error text color contrast ratio       | Error text meets WCAG contrast requirements (4.5:1 min) |
| 5.4 | Non-visual Indicators  | Check non-color error indicators           | Errors use icons/patterns in addition to color coding   |
| 5.5 | Keyboard Navigation    | Test keyboard navigation to error fields   | Error fields can be navigated to via keyboard           |

### 6. Error Message Content Display

| #   | Content Type            | Test Description                        | Expected Behavior                                         |
| --- | ----------------------- | --------------------------------------- | --------------------------------------------------------- |
| 6.1 | Error Message Clarity   | Verify error messages are clear/direct  | Messages explain issue clearly without technical jargon   |
| 6.2 | Solution Guidance       | Check error resolution guidance         | Error messages include steps to resolve when appropriate  |
| 6.3 | Technical Details       | Test display of technical details       | Technical details hidden by default or properly formatted |
| 6.4 | Message Length Handling | Verify handling of long error messages  | Long messages wrap or truncate according to design spec   |
| 6.5 | Message Consistency     | Check terminology consistency in errors | Error terminology is consistent across the application    |

### 7. Error Message Responsiveness

| #   | Screen Size           | Test Description                           | Expected Behavior                                         |
| --- | --------------------- | ------------------------------------------ | --------------------------------------------------------- |
| 7.1 | Mobile Error Display  | Check error display on small screens       | Errors adapt to small screens without text overflow       |
| 7.2 | Tablet Error Display  | Verify error positioning on medium screens | Errors position appropriately for tablet view             |
| 7.3 | Desktop Error Display | Test error appearance on large screens     | Errors utilize space appropriately on desktop views       |
| 7.4 | Multi-column Layout   | Check error display in multi-column forms  | Errors align properly in multi-column layouts             |
| 7.5 | Orientation Changes   | Verify error display on orientation change | Error positioning adjusts correctly on orientation change |

**Post-conditions:**

- All error messages display correctly according to design specifications
- Error message styling is consistent across the application
- Error messages provide clear guidance to help users resolve issues
- Error messages are accessible to all users including those using assistive technologies
- Error displays adapt appropriately to different device sizes and orientations
