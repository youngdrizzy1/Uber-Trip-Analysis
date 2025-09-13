# UBER TRIP ANALYSIS

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Post-blue)](https://www.linkedin.com/posts/eromosele-itoya_powerbi-dataanalysis-uberdata-activity-7372580513133518848-vK4l?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEbDOGsBGINDr5uoWo3fkmNHZc_HI1Qst6k)

### Table of Contents
- [Project Overview](#Project-Overview)
- [Tools](#Tools)
- [Workflow](#Workflow)
- [Insights](#Insights)
- [Recommendations](#Recommendations)
- [Strategic Goals](#Strategic-Goals)
- [Dashboard](#Dashboard)

### Project Overview
This project dives into Uber trip data from June 2024, analyzing over 103.7K bookings to uncover trends in revenue, efficiency, and demand. Using Power BI, I transformed raw datasets into an interactive, multi-page dashboard that highlights key metrics like total revenue ($1.6M), average trip value ($15), and distance (349K miles total, 3 miles avg). The focus was on meeting business needs: spotting booking patterns, optimizing operations, and providing granular insights via drill-throughs. It's not just about the numbers—it's about turning them into actionable strategies for better ride-sharing. How might these patterns shift with seasonal data or in different cities? This setup invites deeper exploration.

### Tools
- Power BI: For data loading, cleaning, modeling, DAX calculations, visualization, and interactive dashboard creation.

### Workflow
I followed a hands-on, iterative process to build a robust dashboard, ensuring every step added value and usability.
#### 1. Data Loading and Cleaning:
- Imported two main datasets: Trip Details (with fields like Trip ID, Pickup Date/Hour, Vehicle, Payment Type, Passengers, Distance, Value, Location) and Location Table (for mapping pickups/drop-offs).
- Handled any duplicates or nulls, formatted dates/times, and categorized trips (e.g., Day/Night based on hour thresholds).
- Created calculated columns for things like Trip Type and ensured data types were consistent for accurate aggregations.
    
#### 2.	Data Modelling and Processing:
- Built relationships between tables (e.g., active link on Pickup Location, inactive for Drop-off to enable switching).
- Developed DAX measures for KPIs: Total Bookings = COUNTROWS(TripDetails), Total Booking Value = SUM(TripDetails[Booking Value]), etc.
- Set up a disconnected table for the Measure Selector (Total Bookings, Total Booking Value, Total Trip Distance) with a dynamic measure to update visuals on the fly.
- Added groupings for analysis: Payment Types (Uber Pay, Cash, etc.), Vehicle Types (UberXL, UberX, Comfort, Black, Green), and time bins (10-min intervals for peaks).

#### 3.	Data Analysis & Visualization:
- Created pivot-like matrices for vehicle analysis with conditional formatting (e.g., red for low revenue, green for high).
- Built charts: Area for pickup time trends, line for daily bookings, heatmap for hour/day demand.
- Implemented enhancements like dynamic titles (e.g., "Total Booking Value by Payment Type"), tooltips with extras (avg values), and slicers for Date, City.
- Added buttons: Clear Filters (resets slicers), Download Raw Data (exports to CSV), and bookmarks for data details pop-ups explaining metrics/sources.

#### 4. Dashboard Assembly:
- Structured into three pages: Overview (KPIs, charts, location insights), Time Analysis (trends, heatmap), Details (drill-through grid).
- Tested interactivity: Drill-through from charts to details, ensuring filters propagate correctly.
- Refined UX with themes, icons, and navigation buttons for seamless flow.

### Insights
Pulling from the data, here are the standout findings—each backed by visuals and raising questions for further digs.
#### 1. Overall Performance:
- Total Bookings: 103.7K | Revenue: $1.6M | Avg Value: $15 | Total Distance: 349K miles | Avg Distance: 3 miles | Avg Time: 16 min.
- Revenue trends show a mid-month peak—perhaps aligned with urban events or pay cycles?

<img width="1270" height="109" alt="KPI" src="https://github.com/user-attachments/assets/1dc62d78-a46c-4889-a788-34eca0d23bd6" />
  
Why might slight injuries dominate? Could early interventions in minor accidents prevent escalation?
  
  <img width="117" height="41" alt="Screenshot (485)" src="https://github.com/user-attachments/assets/b0816b27-ee42-44b7-93b9-460ac4f6ffe1" />

#### 2. Casualties by Vehicle Type
- Cars: 203,357 (79.5%), Bikes: 21,218 (8.3%), Vans: 20,416 (8.0%), Buses: 7,444 (2.9%), Agricultural: 598 (0.2%), Others: 2,831 (1.1%).

Maximum by type: Cars. What role do vehicle volumes versus safety features play?

<img width="255" height="174" alt="Screenshot (486) 1" src="https://github.com/user-attachments/assets/e6d5f229-3d84-4990-8d7a-43617f6b4bfb" />

#### 3.  Monthly Trends (2021 vs. 2022)
- 2021 Total: 134,613 (higher peaks in Nov-Dec).
- 2022 Total: 121,251 (general decline).
- Why the drop? Post-COVID travel changes or improved safety measures?

  <img width="399" height="230" alt="Screenshot (490) 1" src="https://github.com/user-attachments/assets/c350d0f7-f095-4ca1-9d37-5a00b4264ec9" />

#### 4. Light Conditions and Time of Day
- Daylight: 186,161 (72.75%), Darkness: 69,703 (27.25%).
- Does higher daylight volume reflect more traffic, or overlooked risks like distractions?
  
<img width="321" height="313" alt="Screenshot (493)1" src="https://github.com/user-attachments/assets/1421daef-e994-4a65-a1f9-37b5e721fa27" />

#### 5.  Road Type and Surface Distribution
- Road Types: Single carriageway (196,600, 76.85%), Dual (32,400, 12.66%), Roundabout (17,200, 6.72%).
- Surfaces: Dry (181,484, 70.91%), Wet (64,567, 25.23%), Ice/Snow (9,813, 3.83%).
- Notice correlations: Most on dry, single carriageways. How might weather interact with infrastructure?

  <img width="240" height="108" alt="Screenshot (492)1" src="https://github.com/user-attachments/assets/1cc427ce-948c-4942-83c3-92416a77864e" />
  <img width="257" height="178" alt="Screenshot (491)1" src="https://github.com/user-attachments/assets/c9165707-b29a-4400-86ea-637aa4a30e9a" />

#### 6. Location Focus
- All visualized data filtered to urban areas (255,864). Why prioritize urban? Higher density amplifies risks.

### Recommendations
Based on patterns, consider:
- Target car safety campaigns, as they dominate casualties. What tech like auto-braking could help?
- Boost awareness for daylight driving risks, perhaps via apps alerting to high-traffic times.
- Improve single carriageway infrastructure (e.g., better lighting on wet surfaces) to address 76.85% of incidents.
- Use monthly trends for seasonal alerts, focusing on winter peaks.
- Expand analysis to rural data for comprehensive views.

### Strategic Goals
- Empower stakeholders (governments, insurers) with data for targeted interventions.
- Reduce overall casualties by 10-20% through evidence-based policies.
- Promote data literacy in road safety to build community-driven changes.
- Foster ongoing analysis for long-term trends, like post-2022 updates.

### Dashboard
The interactive Excel dashboard summarizes all insights with filters for customization.
