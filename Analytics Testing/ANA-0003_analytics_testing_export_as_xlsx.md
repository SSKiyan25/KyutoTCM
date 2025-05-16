## **ANA-0003:** Analytics testing - Export as XLSX

> **Summary:** Verify that organization users can export analytics sections (Sales Trend, Pre-Order vs Direct Order pie chart, and Top Products) as XLSX (Excel) files.

**Preconditions:**

- User must be logged in as an organization.
- Organization must have sales data recorded in the system.
- User must have permission to access the analytics dashboard.

Scenario 1: Export Sales Trend as XLSX

| #   | Step                                                                                                                 | Expected Behavior                                                                                 |
| --- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| 1   | Launch application.                                                                                                  | Verify that the home screen is shown.                                                             |
| 2   | For desktop, click the `Dashboard` link in the sidebar.                                                              | Verify that the Dashboard page with analytics is displayed.                                       |
| 3   | For mobile, click the `Dashboard` link in the footer or tap the burger icon and select `Dashboard` from the sidebar. | Verify that the Dashboard page with analytics is displayed.                                       |
| 4   | Locate the Sales Trend section on the Dashboard.                                                                     | Verify that the Sales Trend chart/graph is visible.                                               |
| 5   | Locate the export button in the Sales Trend section.                                                                 | Verify that the export button is visible and clickable.                                           |
| 6   | Click on the export button.                                                                                          | Verify that the export options appear.                                                            |
| 7   | Select "Export as XLSX" from the options.                                                                            | Verify that the Sales Trend data is exported as an XLSX file and downloaded to the user's device. |
| 8   | Open the downloaded XLSX file using Microsoft Excel or compatible software.                                          | Verify that the Excel file displays the Sales Trend data correctly as shown on the dashboard.     |

Scenario 2: Export Pre-Order vs Direct Order Pie Chart as XLSX

| #   | Step                                                                             | Expected Behavior                                                                                                                         |
| --- | -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | From the Dashboard page, locate the Pre-Order vs Direct Order pie chart section. | Verify that the pie chart is visible.                                                                                                     |
| 2   | Locate the export button in the Pre-Order vs Direct Order section.               | Verify that the export button is visible and clickable.                                                                                   |
| 3   | Click on the export button.                                                      | Verify that the export options appear.                                                                                                    |
| 4   | Select "Export as XLSX" from the options.                                        | Verify that the pie chart data is exported as an XLSX file and downloaded to the user's device.                                           |
| 5   | Open the downloaded XLSX file using Microsoft Excel or compatible software.      | Verify that the Excel file displays the Pre-Order vs Direct Order data correctly, including raw data and possibly a chart representation. |

Scenario 3: Export Top Products as XLSX

| #   | Step                                                                        | Expected Behavior                                                                                                                                  |
| --- | --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | From the Dashboard page, locate the Top Products section.                   | Verify that the Top Products list/chart is visible.                                                                                                |
| 2   | Locate the export button in the Top Products section.                       | Verify that the export button is visible and clickable.                                                                                            |
| 3   | Click on the export button.                                                 | Verify that the export options appear.                                                                                                             |
| 4   | Select "Export as XLSX" from the options.                                   | Verify that the Top Products data is exported as an XLSX file and downloaded to the user's device.                                                 |
| 5   | Open the downloaded XLSX file using Microsoft Excel or compatible software. | Verify that the Excel file displays the Top Products data correctly, including product names, quantities, sales figures, and any relevant metrics. |

**Post-conditions:**

- Analytics sections (Sales Trend, Pre-Order vs Direct Order pie chart, and Top Products) can be exported as XLSX (Excel) files.
- The exported XLSX files accurately reflect the data shown on the dashboard.
- Users can download and view the exported Excel files using Microsoft Excel or compatible software.
- The Excel files contain properly formatted data that can be used for further analysis or reporting.
