# Marketing & Operations BI Dashboard



**Dashboard demo** (watch first):  
[Dashboard Demo](
*(~1–2 minutes – shows dashboard navigation, slicers, KPIs, and trend visuals)*

## Project Overview

This project simulates the work of a **Business Intelligence Analyst** at **Faebl Studios** — a marketing & technology company specializing in SEO, PPC, web design, and full-funnel strategies for addiction treatment facilities.

**Purpose of the system**  
Build a clean, refreshable Excel dashboard that turns complex marketing & operational data (Google Ads, CallTrackingMetrics, Salesforce CRM) into **accurate, actionable insights** for internal teams and clients — helping treatment centers reach more people in need through better decision-making.

## Critical Steps (Documented with Photos)

1. **Data Import & Load to Data Model**  
   Imported synthetic Google Ads, CTM, and Salesforce (companies + employees) tables.  
   Loaded each to **Data Model** using **Only Create Connection + Add to Data Model**.  
   → Photo: [Screenshot of Queries & Connections pane showing 4 connections]

2. **Synthetic GCLID Creation & Propagation**  
   Generated unique GCLID in Google Ads (source of truth).  
   Copied realistic subset (~35% to CTM, ~20% to CRM Employees) to simulate attribution funnel.  
   → Photo: [Power Query step showing GCLID formula + preview of unique values]

3. **Relationships in Data Model**  
   Created one-to-many relationships:  
   - Google Ads [GCLID] (1) → CTM [GCLID] (*)  
   - CTM [GCLID] (*) → Employees [GCLID] (1)  
   - Companies [Company_ID] (1) → Employees [Company_ID] (*)  
   → Photo: [Diagram View screenshot showing all 3 relationships with arrows]

4. **KPI Cards (6 Core Metrics)**  
   Built using PivotTables + DAX measures:  
   - Total Leads MTD  
   - Conversion Rate  
   - Cost Per Lead  
   - Total Admissions  
   - Average Call Duration  
   - Client ROI  
   → Photo: [Dashboard screenshot of the 6 formatted KPI cards]

5. **Main Visuals**  
   - Monthly Lead Generation & Admissions Trend (combo chart)  
   - Call Performance Metrics (stacked column/table: Answered, Missed, After Hours, Transferred)  
   → Photo: [Trend chart + Call Performance table]

6. **Interactivity & Final Polish**  
   Connected slicers (Month, Campaign, Industry, Job Title) to all visuals.  
   Applied conditional formatting (green/red), consistent branding, and refresh notes.  
   → Photo: [Full dashboard view with slicers active]

## Tools & Technologies Used

- Excel (Microsoft 365)  
- Power Query (data cleaning & GCLID creation)  
- Power Pivot / Data Model (relationships & DAX)  
- DAX measures for KPIs (e.g. ROI, Conversion Rate)  
- PivotTables + PivotCharts + Slicers for visuals

## Limitations & Notes

- Excel Data Model uses **single-direction filtering** only (one → many).  
  Reverse filtering (CTM → CRM) simulated with DAX when needed.
- All GCLID values are synthetic (random 19-digit strings).
- Designed for internal & client-facing reporting — no real client data included.

## Future Improvements

- Add more visuals (Top Keywords by Cost per Lead, Lead Source Breakdown)
- Move to Power BI Desktop for true bidirectional filtering
- Automate monthly refresh via Power Automate
- Export to PDF/PowerPoint for client delivery

## Author

Ali  
Business Intelligence Analyst (simulated role for Faebl Studios project)

Last updated: February 2026

