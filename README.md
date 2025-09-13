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
  
#### 2. Payment and Trip Types
- Uber Pay: 67% (70K bookings), Cash: 32% (33K), Google Pay minimal.
- Day Trips: 65% (68K), Night: 35% (35K)—but nights have slightly higher avg values ($15.5 vs. $14.8). Why the premium at night?

<img width="632" height="297" alt="Screenshot 2025-09-13 110315" src="https://github.com/user-attachments/assets/09b8e42b-c6a4-447e-ac77-4aed164417de" />

#### 3.  Vehicle Type Breakdown
- UberXL: 16.7K bookings, $249K revenue, 57.5K miles.
- UberX: 38.7K bookings, $583K revenue (highest overall).
- Others like Comfort ($253K) show premium appeal, but Green underperforms—eco trends not catching on yet?

<img width="632" height="294" alt="Vehicle" src="https://github.com/user-attachments/assets/b157f099-9880-4f1a-9531-f1a9b80c44f4" />

#### 4. Time and Daily Trends
- Peaks at 10-11 AM and 5-6 PM; heatmap shows Friday evenings as hottest.
- Bookings by day: Wednesday highest ($239K), Sunday lowest ($224K). Weekend mornings surprise with steady demand.
  
<img width="571" height="545" alt="Time" src="https://github.com/user-attachments/assets/207fb536-fce5-4c9a-af16-e4d511e06aa6" />

<img width="680" height="546" alt="Heatmap" src="https://github.com/user-attachments/assets/ed259ca2-e3b4-421d-8f18-9f167dfb2b4d" />

#### 5.  Location Insights
- Top Pickup: Penn Station/Madison Sq West (4.5K bookings).
- Top Drop-off: Upper East Side North (4.1K).
- Farthest: 144.1 miles (Lower East Side → Crown Heights).
- Preferred Vehicles: UberX for most urban pickups, XL for airports like JFK.

![Location](https://github.com/user-attachments/assets/96084b34-b80e-4bdf-ad9c-7903fc1d248d)

#### 6. Granular Details
- Sample trips: Short 1-mile cash rides in East Village ($7-9), longer 12-mile airport hauls ($36+).
- Total across sample: 14.6K bookings in details view, summing to $153K.

### Recommendations
Drawing from the insights:
- Optimize for peaks: Surge pricing during 5-6 PM Fridays; allocate more drivers to Penn Station.
- Promote underperformers: Incentives for Green vehicles in eco-conscious areas like Upper East Side.
- Enhance efficiency: Analyze long trips for route optimizations; test dynamic pricing based on day/night splits.
- Expand data: Integrate weather or event data to explain fluctuations—could boost predictive accuracy.
- User-focused: Add mobile optimization to the dashboard for on-the-go stakeholder access.

### Strategic Goals
- Equip Uber-like ops with tools to increase revenue by 10-15% through better demand forecasting.
- Improve rider/driver experiences by reducing wait times in hotspots.
- Build a scalable template for similar analyses (e.g., Lyft data or multi-city expansions).
- Encourage data-driven culture in mobility, fostering collaborations with urban planners or insurers.

### Dashboard
The Power BI dashboard is fully interactive with slicers, drill-throughs, and dynamic elements. Screenshots below; PBIX file available in the repo for exploration.
- ####  Overview Analysis:
![Dashboard_Overview](https://github.com/user-attachments/assets/7b1ec097-6d85-4d23-8c4b-1f8ea35acc62)

- #### Time Analysis:
<img width="1443" height="809" alt="Screenshot 2025-09-13 110330" src="https://github.com/user-attachments/assets/cd65f329-9095-47ff-92ae-a49df165ee0a" />

- #### Details Analysis:
<img width="1427" height="803" alt="Screenshot 2025-09-13 110342" src="https://github.com/user-attachments/assets/6d3f09f5-7e5f-4589-840c-b6982c3fecb4" />

## Connect with Me 👋
[LinkedIn](https://www.linkedin.com/in/eromosele-itoya/) | 
[GitHub](https://github.com/youngdrizzy1)
