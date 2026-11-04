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

##################################################################################################################################################################

## Application Journey and Marketing Channel Analysis

Built an Adobe Customer Journey Analytics (CJA) dashboard using training data to investigate application progression, identify drop-off, and compare marketing channels.

![Application Progression by Marketing Channel](images/application-progression-by-channel.png)

### Business Questions

- What proportion of sessions progress from application step 1 to step 2?
- How does progression compare between the original application and mobile web page sequences?
- How does progression vary across marketing channels?

### Approach

- Created session-based Fallout visualizations using **Eventual Path**, allowing intervening events between steps.
- Built reusable segments for sessions reaching step 1 and sessions reaching step 1 followed by step 2.
- Created a calculated metric:

  **Progression Rate = Sessions progressing from step 1 to step 2 ÷ Sessions reaching step 1**

- Compared session volume and progression rates by Marketing Channel.
- Validated table totals against the funnel and aligned reporting dates to November 1–3, 2026.

### Findings

| Application sequence | Step 1 sessions | Progressed to step 2 | Progression rate | Drop-off rate |
|---|---:|---:|---:|---:|
| Original application | 28,479 | 9,290 | 32.6% | 67.4% |
| Mobile web | 3,051 | 976 | 32.0% | 68.0% |

Email had the highest step 1 session volume among the reported channels, with 32.7% progression. Push progression was 32.8%, compared with 31.4% for Natural Search.

### Interpretation and Next Steps

Approximately two-thirds of qualifying sessions did not progress to step 2. Further investigation should examine form errors, navigation, and user experience across both application sequences.

The 0.6 percentage point difference does not establish a mobile-specific problem.

### Scope and Limitations

This project uses training data. Step 2 has not been verified as a completed application, and the original application sequence has not been confirmed as desktop-only. Sessions may appear under multiple marketing channels; these comparisons do not establish causation or incremental channel impact.

**Skills demonstrated:** Analysis Workspace, Fallout analysis, sequential session segments, calculated metrics, marketing channel analysis, data validation, and business interpretation.
See the image Application Progression by Marketing Channel.png for the visualization.
