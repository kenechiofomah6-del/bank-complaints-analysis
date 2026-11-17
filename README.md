# Nigerian Bank Complaints Analysis

A project exploring complaint trends, resolution outcomes, and service-level agreement (SLA) performance across selected Nigerian banks using.

**Author:** Kenechi Ofomah  
**Tools:** Microsoft Excel, Power Query, and Power BI  
**Dataset:** 50,000 complaint records covering 1 January 2023 to 28 July 2026

## Business questions

- How many complaints and unique customers are represented?
- Which complaint categories and text themes are most common?
- How does complaint volume vary over time, by bank, and by state?
- How many complaints are high or critical priority or are flagged as suspected fraud?
- What share of complaints were completed or breached their SLA, and how do these measures vary by bank?

## Data preparation

1. Checked all 50,000 complaint IDs for duplicates and confirmed that the cleaned data retained all records.
2. Standardised the transaction amount column as `Transaction_Amount_NGN`. Removed currency symbols, commas, and surrounding spaces, then converted 37,562 populated amounts to numeric values.
3. Converted `Date_Received` and `Transaction_Date` to date fields. Preserved blank transaction details in 12,438 records because those complaints were not tied to a specific transaction.
4. Added `Text_Theme` to group free-text complaint descriptions into broader themes.
5. Built a separate date table in Power BI for chronological filtering and created measures for complaint counts, completion, and SLA breaches.

## Dashboard

| Page | What it shows |
| --- | --- |
| **Nigerian Bank Complaints Analysis** | Six KPI cards, a monthly trend, and complaint volumes by category, bank, and state. Use the date and bank filters to explore the results. |
| **Complaint Operations, SLA, and Bank Performance** | Complaint status and text themes, plus a bank comparison matrix with conditional formatting for completion, SLA breaches, and suspected fraud. |

### Measure definitions

- **Completed complaints** include records marked `Resolved` or `Closed`.
- **SLA breaches** include records marked `Breached` or `Open - Breached`.

## How to view the dashboard

Open the project’s `.pbix` file in Microsoft Power BI Desktop. Use the page tabs to switch between the overview and the operations dashboard.

