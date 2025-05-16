## **ANA-0002:** Analytics testing - Export as PDF

> **Summary:** Verify that organization users can export analytics sections (Sales Trend, Pre-Order vs Direct Order pie chart, and Top Products) as PDF.

**Preconditions:**

- User must be logged in as an organization.
- Organization must have sales data recorded in the system.
- User must have permission to access the analytics dashboard.

Scenario 1: Export Sales Trend as PDF

| #   | Step                                                                                                                 | Expected Behavior                                                                               |
| --- | -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                  | Verify that the home screen is shown.                                                           |
| 2   | For desktop, click the `Dashboard` link in the sidebar.                                                              | Verify that the Dashboard page with analytics is displayed.                                     |
| 3   | For mobile, click the `Dashboard` link in the footer or tap the burger icon and select `Dashboard` from the sidebar. | Verify that the Dashboard page with analytics is displayed.                                     |
| 4   | Locate the Sales Trend section on the Dashboard.                                                                     | Verify that the Sales Trend chart/graph is visible.                                             |
| 5   | Locate the export button in the Sales Trend section.                                                                 | Verify that the export button is visible and clickable.                                         |
| 6   | Click on the export button.                                                                                          | Verify that the export options appear.                                                          |
| 7   | Select "Export as PDF" from the options.                                                                             | Verify that the Sales Trend data is exported as a PDF file and downloaded to the user's device. |
| 8   | Open the downloaded PDF file.                                                                                        | Verify that the PDF displays the Sales Trend data correctly as shown on the dashboard.          |

Scenario 2: Export Pre-Order vs Direct Order Pie Chart as PDF

| #   | Step                                                                             | Expected Behavior                                                                                              |
| --- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| 1   | From the Dashboard page, locate the Pre-Order vs Direct Order pie chart section. | Verify that the pie chart is visible.                                                                          |
| 2   | Locate the export button in the Pre-Order vs Direct Order section.               | Verify that the export button is visible and clickable.                                                        |
| 3   | Click on the export button.                                                      | Verify that the export options appear.                                                                         |
| 4   | Select "Export as PDF" from the options.                                         | Verify that the pie chart data is exported as a PDF file and downloaded to the user's device.                  |
| 5   | Open the downloaded PDF file.                                                    | Verify that the PDF displays the Pre-Order vs Direct Order pie chart data correctly as shown on the dashboard. |

Scenario 3: Export Top Products as PDF

| #   | Step                                                      | Expected Behavior                                                                                |
| --- | --------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| 1   | From the Dashboard page, locate the Top Products section. | Verify that the Top Products list/chart is visible.                                              |
| 2   | Locate the export button in the Top Products section.     | Verify that the export button is visible and clickable.                                          |
| 3   | Click on the export button.                               | Verify that the export options appear.                                                           |
| 4   | Select "Export as PDF" from the options.                  | Verify that the Top Products data is exported as a PDF file and downloaded to the user's device. |
| 5   | Open the downloaded PDF file.                             | Verify that the PDF displays the Top Products data correctly as shown on the dashboard.          |

**Post-conditions:**

- Analytics sections (Sales Trend, Pre-Order vs Direct Order pie chart, and Top Products) can be exported as PDF.
- The exported PDFs accurately reflect the data shown on the dashboard.
- Users can download and view the exported PDFs.
