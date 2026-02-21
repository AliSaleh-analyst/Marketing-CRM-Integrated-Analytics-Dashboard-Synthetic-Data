# Marketing & Operations BI Dashboard

**Dashboard demo** (watch first):  
![gif](https://github.com/user-attachments/assets/9406340c-db42-4f17-a41b-c6fd4efdc156)


## Project Overview

This project simulates the work of a **Business Intelligence Analyst** at **X Company**; a marketing & technology company specializing in SEO, PPC, web design, and full-funnel strategies for addiction treatment facilities.

**Purpose of the system**  
Build a clean, refreshable Excel dashboard that turns complex marketing & operational data (Google Ads, CallTrackingMetrics, Salesforce CRM) into **accurate, actionable insights** for internal teams and clients; helping treatment centers reach more people in need through better decision-making.

## Critical Steps (Documented with Photos)
1. **Data Cleaning**
   Standardized text (trim/clean), fixed typos (bulk replace), corrected time format, removed duplicates on keys.
   
   <img width="975" height="543" alt="image" src="https://github.com/user-attachments/assets/977bcb45-8b4e-4bb2-a87e-f4629be2ecf3" />
   <img width="975" height="575" alt="image" src="https://github.com/user-attachments/assets/70480fa9-83e5-4ba9-94b9-a86433b4b044" />


3. **Data Import & Load to Data Model**  
   Imported synthetic Google Ads, CTM, and Salesforce (companies + employees) tables.  
   Loaded each to **Data Model** using **Only Create Connection + Add to Data Model**.  

    <img width="435" height="731" alt="image" src="https://github.com/user-attachments/assets/3b4f5889-2f75-4442-8e7a-a724f1544add" />


5. **Synthetic GCLID Creation & Propagation**  
   Generated unique GCLID in Google Ads (source of truth).  
   Copied realistic subset (~35% to CTM, ~20% to CRM Employees) to simulate attribution funnel.  

   <img width="326" height="111" alt="image" src="https://github.com/user-attachments/assets/c74fdfe3-fa14-4d42-8d53-61d6326cc3d4" />


6. **Relationships in Data Model**  
   Created one-to-many relationships to build a Star Schema:  

<img width="1740" height="853" alt="image" src="https://github.com/user-attachments/assets/0a4a9737-6e2a-4da4-9db0-019f375dd182" />


7. **KPI Cards (6 Core Metrics)**  
   Built using PivotTables + DAX measures:  
   - Total Leads MTD  
   - Conversion Rate  
   - Cost Per Lead  
   - Total Admissions  
   - Average Call Duration  
   - Client ROI  

   <img width="1733" height="72" alt="image" src="https://github.com/user-attachments/assets/c7a77bd9-a1bb-468e-8746-504441f6c42e" />


8. **Main Visuals**  
   - Monthly Lead Generation & Admissions Trend (combo chart)  
   - Contact Channels Distributions
   - Geographic Distribution
   - Calls Peak Times

   <img width="1619" height="729" alt="image" src="https://github.com/user-attachments/assets/0918ebb5-45ac-4e34-9036-1cf1dd0f5351" />


9. **Interactivity & Final Polish**  
   Connected slicers (Month, Campaign, Calls Satisfaction) to all visuals.  
   
   <img width="220" height="593" alt="image" src="https://github.com/user-attachments/assets/edbb35f8-a1a0-4425-abd0-e52fdc6a8c8b" />


## Tools & Technologies Used

- Excel (Microsoft 365)  
- Power Query (data cleaning & GCLID creation)  
- Power Pivot / Data Model (relationships & DAX)  
- DAX measures for KPIs (e.g. ROI, Conversion Rate)  
- PivotTables + PivotCharts + Slicers for visuals

## Limitations & Notes

- All GCLID values are synthetic (random 19-digit strings).
- Designed for internal & client-facing reporting — no real client data included.


## Author

Ali  
Business Intelligence Analyst (simulated role for X company project)

Last updated: February 2026

