# 🚖 Ride-Sharing Analytics Dashboard (Ola Dataset)

## 📌 Project Overview
This project analyzes ride-sharing data from the Ola dataset to derive actionable insights about booking trends, cancellations, ride distances, customer behavior, and revenue distribution. Using **SQL** for data querying and **Power BI** for visualization, it delivers an end-to-end analytics solution to support data-driven decision-making for ride-sharing businesses.

## 🎯 Objectives
- Analyze over 100,000 ride records to understand booking patterns and customer behavior.
- Identify top vehicle types, peak booking times, and cancellation reasons.
- Optimize revenue insights based on payment methods and demand trends.
- Build an interactive **Power BI dashboard** for stakeholders to explore key performance indicators (KPIs) visually.

## 🛠️ Tech Stack
- **Database & Querying:** SQL (MySQL / PostgreSQL)
- **Data Visualization:** Power BI
- **Data Preparation:** Excel / Python (optional for cleaning)
- **Version Control:** Git, GitHub

## 📊 Key Features & Analysis
- **Booking Status Breakdown:** Success vs. cancellations (customer/driver)
- **Ride Trends Over Time:** Peak days, weekends, and special events
- **Vehicle Type Performance:** Distance traveled & customer preference
- **Customer & Driver Ratings:** Distribution and correlation
- **Revenue Insights:** Total booking value by payment method

## 📂 Project Structure
Ride-Sharing-Analytics-Dashboard/
│
├── data/                    # Raw and cleaned Ola dataset
├── sql_queries/             # SQL scripts (views, aggregations, joins)
│   ├── successful_bookings.sql
│   ├── top_customers.sql
│   └── avg_distance_by_vehicle.sql
├── powerbi_dashboard/       # Power BI (.pbix) file with visuals
├── reports/                 # Exported PDF/PNG reports for quick view
└── README.md                # Project documentation


## 📌 Example SQL Queries
```sql
-- Retrieve all successful bookings
SELECT * FROM bookings WHERE Booking_Status = 'Success';

-- Find the average ride distance for each vehicle type
SELECT Vehicle_Type, AVG(Ride_Distance) AS avg_distance
FROM bookings
GROUP BY Vehicle_Type;

-- List top 5 customers with maximum bookings
SELECT Customer_ID, COUNT(Booking_ID) AS total_rides
FROM bookings
GROUP BY Customer_ID
ORDER BY total_rides DESC
LIMIT 5;
```
## 📧 Author
Chetan Raval
