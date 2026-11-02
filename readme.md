In Adobe’s October 2026 sample data, Email had the highest attributed online order volume, while In-App Messaging recorded approximately 2.2 times Email’s orders per session among the channels displayed.

See Visualization.png for details.

## Claims Risk Profile Analysis - see Claims.png for visualization

Explored insurance-related CRM profile fields in Adobe Customer Journey Analytics (CJA), using the **Omni-Channel – Multi-Industry** sample data view.

### Objective

Examine how people are distributed across recorded claim risk categories and explore whether recorded Claims Filed YTD values differ across those groups.

### Tools and Methods

- Built Freeform tables and a horizontal bar chart in Analysis Workspace.
- Used the **People** metric to count distinct people associated with each claim risk status.
- Created nested breakdowns of **Claims Filed YTD** within Low, Medium, and High risk groups.
- Exported CSV files to compare the recorded values and validate reporting totals.

### Findings

The risk-status table returned the following results for November 1–30, 2026:

| Claim Risk Status | People |
|---|---:|
| Medium | 33,736 |
| Low | 11,676 |
| High | 10,413 |
| No value | 28,199 |

The most common populated Claims Filed YTD value was **27** in all three risk groups. Exploratory comparisons showed similar recorded-value patterns across the groups, without a clear separation based on this field alone.

The final dashboard retains the risk-status chart and its supporting table. Detailed YTD breakdowns were used for exploration.

### Interpretation and Limitations

- This is an independent practice project using Adobe sample data
- People counts represent individuals associated with field values, rather than counts of claims.
- The sample does not document the risk-scoring rules or fully define Claims Filed YTD.
- “No value” represents an unavailable classification in the report. It does not mean zero claims. Because the dataset spans multiple industries, it may also include people for whom insurance fields are not applicable.
- Breakdown totals exceeded parent-level distinct-person counts. Counts across recorded values should therefore not be added or treated as a mutually exclusive customer distribution.
- The analysis is descriptive and does not establish fraud risk, claim severity, retention outcomes, or causation.

### Skills Demonstrated

Adobe CJA Analysis Workspace, data visualization, profile segmentation, dimension breakdowns, CSV export, metric validation, and communicating analytical limitations.
