## **UI-0008:** UI Messages Testing - Helper Texts

> **Summary:** Verify that helper texts in various parts of the application are displayed correctly, provide relevant guidance, and follow the design guidelines in https://github.com/SSKiyan25/kyuto.

**Preconditions:**

- Tester has access to the KyutoTCM application
- Tester has appropriate permissions to access all application sections

### 1. Form Field Helper Texts

| #   | Location                  | Test Description                        | Expected Behavior                                           |
| --- | ------------------------- | --------------------------------------- | ----------------------------------------------------------- |
| 1.1 | Input Field Helper Text   | Verify helper text below input fields   | Text appears with proper styling, spacing, and information  |
| 1.2 | Required Field Indicators | Check required field helper text        | Required field indicators display with proper styling       |
| 1.3 | Password Requirements     | Verify password requirement helper text | Password criteria displays clearly with appropriate styling |
| 1.4 | Field Character Limits    | Test maximum length indicator text      | Character count/limit displays with proper styling          |
| 1.5 | Date Format Guidelines    | Check date format helper text           | Date format examples display with clear formatting          |
| 1.6 | Input Format Examples     | Verify example input helper text        | Example inputs display with appropriate styling             |

### 2. Tooltip Helper Texts

| #   | Location                  | Test Description                     | Expected Behavior                                      |
| --- | ------------------------- | ------------------------------------ | ------------------------------------------------------ |
| 2.1 | Field Label Tooltips      | Check tooltips on form field labels  | Tooltips display on hover/click with proper styling    |
| 2.2 | Icon Information Tooltips | Verify tooltips on information icons | Icon tooltips display with clear, helpful content      |
| 2.3 | Action Button Tooltips    | Test tooltips on action buttons      | Button tooltips explain actions clearly                |
| 2.4 | Setting Option Tooltips   | Check tooltips for setting options   | Setting tooltips provide relevant guidance             |
| 2.5 | Disabled Control Tooltips | Verify tooltips on disabled controls | Tooltips explain why controls are disabled             |
| 2.6 | Advanced Feature Tooltips | Test tooltips for advanced features  | Advanced feature tooltips provide adequate explanation |

### 3. Section Introduction Texts

| #   | Location                  | Test Description                        | Expected Behavior                                          |
| --- | ------------------------- | --------------------------------------- | ---------------------------------------------------------- |
| 3.1 | Dashboard Section Intros  | Check section introduction text         | Introductory text displays with proper styling and content |
| 3.2 | Form Section Headers      | Verify form section helper text         | Section explanations provide clear guidance                |
| 3.3 | Settings Category Intros  | Test settings section introduction text | Intro text explains settings category purpose              |
| 3.4 | Feature Introduction Text | Check new feature introduction helpers  | New feature explanations provide clear guidance            |
| 3.5 | Report Introduction Text  | Verify analytics/report section intros  | Report introduction explains available data and filters    |

### 4. Placeholder Text

| #   | Location                  | Test Description                       | Expected Behavior                                             |
| --- | ------------------------- | -------------------------------------- | ------------------------------------------------------------- |
| 4.1 | Input Field Placeholders  | Check placeholder text in input fields | Placeholders display with proper styling and helpful examples |
| 4.2 | Search Field Placeholders | Verify search field placeholder text   | Search placeholder provides clear guidance on search scope    |
| 4.3 | Dropdown Placeholders     | Test dropdown default/placeholder text | Dropdown placeholders indicate selection requirements         |
| 4.4 | Textarea Placeholders     | Check text area placeholder styling    | Textarea placeholders provide guidance on expected content    |
| 4.5 | Default Selection Text    | Verify default selection text          | Default selection text is clear and properly styled           |

### 5. Contextual Help Texts

| #   | Location                 | Test Description                           | Expected Behavior                                          |
| --- | ------------------------ | ------------------------------------------ | ---------------------------------------------------------- |
| 5.1 | Workflow Step Guidance   | Check step-by-step helper text             | Step guidance provides clear instructions for current step |
| 5.2 | Feature Introduction     | Verify first-time use helper text          | First use guidance explains feature purpose and usage      |
| 5.3 | Form Completion Guidance | Test form completion helper text           | Form guidance provides tips for successful completion      |
| 5.4 | Data Input Guidelines    | Check contextual data input help           | Data guidelines explain expected formats and requirements  |
| 5.5 | Action Consequence Text  | Verify text explaining action consequences | Consequence explanations clearly indicate what will happen |

### 6. Empty State Helper Texts

| #   | Location                 | Test Description                         | Expected Behavior                                           |
| --- | ------------------------ | ---------------------------------------- | ----------------------------------------------------------- |
| 6.1 | Empty List Helper Text   | Check helper text for empty lists/tables | Empty state text explains why list is empty with next steps |
| 6.2 | No Results Helper Text   | Verify no search results helper text     | No results text provides guidance on broadening search      |
| 6.3 | Getting Started Text     | Test first-time section helper text      | Getting started text provides clear first steps             |
| 6.4 | No Data Helper Text      | Check analytics with no data helper text | No data text explains how to generate reportable data       |
| 6.5 | First Item Creation Help | Verify guidance for creating first item  | First creation help provides clear process guidance         |

### 7. Helper Text Responsiveness

| #   | Screen Size              | Test Description                                 | Expected Behavior                                          |
| --- | ------------------------ | ------------------------------------------------ | ---------------------------------------------------------- |
| 7.1 | Mobile Helper Text       | Check helper text display on small screens       | Helper text remains visible and readable on mobile devices |
| 7.2 | Tablet Helper Text       | Verify helper text positioning on medium screens | Helper text adjusts position appropriately for tablets     |
| 7.3 | Desktop Helper Text      | Test helper text appearance on large screens     | Helper text utilizes available space without overwhelming  |
| 7.4 | Tooltip Responsiveness   | Check tooltip positioning across screen sizes    | Tooltips position correctly without overflow issues        |
| 7.5 | Long Helper Text Display | Verify how long helper text adapts               | Long text handles wrapping and truncation appropriately    |

**Post-conditions:**

- All helper texts display correctly according to design specifications
- Helper texts provide relevant guidance to users
- Helper text styling is consistent across the application
- Text remains readable and accessible across device sizes
