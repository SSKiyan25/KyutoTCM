## **ANA-0001:** Analytics testing - Filter Sales Trend

> **Summary:** Verify that organization users can filter sales trend analytics by different time periods.

**Preconditions:**

- User must be logged in as an organization.
- Organization must have sales data recorded in the system.
- User must have permission to access the analytics dashboard.

Scenario 1

| #   | Step                                                                                                                 | Expected Behavior                                                                    |
| --- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| 1   | Launch application.                                                                                                  | Verify that the home screen is shown.                                                |
| 2   | For desktop, click the `Dashboard` link in the sidebar.                                                              | Verify that the Dashboard page with analytics is displayed.                          |
| 3   | For mobile, click the `Dashboard` link in the footer or tap the burger icon and select `Dashboard` from the sidebar. | Verify that the Dashboard page with analytics is displayed.                          |
| 4   | Locate the Sales Trend section on the Dashboard.                                                                     | Verify that the Sales Trend chart/graph is visible.                                  |
| 5   | Locate the filter dropdown in the Sales Trend section.                                                               | Verify that the filter dropdown is visible and clickable.                            |
| 6   | Click on the filter dropdown.                                                                                        | Verify that filter options appear: Last 30 days, A week, A month, A Quarter, A year. |
| 7   | Select "Last 30 days" from the dropdown.                                                                             | Verify that the Sales Trend graph updates to show data for the last 30 days.         |
| 8   | Click on the filter dropdown again.                                                                                  | Verify that filter options appear.                                                   |
| 9   | Select "A week" from the dropdown.                                                                                   | Verify that the Sales Trend graph updates to show data for the last week.            |
| 10  | Click on the filter dropdown again.                                                                                  | Verify that filter options appear.                                                   |
| 11  | Select "A month" from the dropdown.                                                                                  | Verify that the Sales Trend graph updates to show data for the last month.           |
| 12  | Click on the filter dropdown again.                                                                                  | Verify that filter options appear.                                                   |
| 13  | Select "A Quarter" from the dropdown.                                                                                | Verify that the Sales Trend graph updates to show data for the last quarter.         |
| 14  | Click on the filter dropdown again.                                                                                  | Verify that filter options appear.                                                   |
| 15  | Select "A year" from the dropdown.                                                                                   | Verify that the Sales Trend graph updates to show data for the last year.            |

**Post-conditions:**

- Sales Trend analytics can be filtered by different time periods: Last 30 days, A week, A month, A Quarter, and A year.
- The graph/chart updates correctly to reflect the selected time period.
- The selected filter option should be displayed as the current selection in the dropdown.
