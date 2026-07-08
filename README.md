# 🚚 Logistics Operations Analytics Dashboard | Power BI
# Project Overview
The Logistics Operations Analytics Dashboard is a comprehensive Power BI solution designed to monitor and optimize end-to-end logistics operations. The dashboard provides actionable insights into order fulfillment, hub performance, driver efficiency, fleet utilization, delivery timeliness, and customer satisfaction.

Built using a star-schema data model and interactive visualizations, the solution enables logistics managers and operations teams to identify bottlenecks, improve delivery performance, optimize resource allocation, and enhance customer experience through data-driven decision-making.

## 🎯 Project Objective
Logistics organizations handle thousands of deliveries daily across multiple hubs, drivers, and vehicles. Tracking operational efficiency manually becomes challenging as the network grows.

This dashboard was developed to answer critical business questions such as:
- How many orders are being processed each month?
- Are deliveries being completed on time?
- Which hubs are operating beyond their capacity?
- Which drivers contribute most to delivery delays?
- How does driver experience impact performance?
- Which vehicles are most prone to breakdowns?
- How efficiently is the fleet being utilized?
- How satisfied are customers with delivery services?
  
The goal is to provide a centralized analytics platform that transforms raw operational data into meaningful business insights.

## 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| 📊 Power BI Desktop | Dashboard Development & Visualization |
| 📂 Power Query | Data Cleaning & Transformation |
| 🧠 DAX | KPI Calculations & Time Intelligence |
| 🔗 Data Modeling | Star Schema Design |
| 📅 Date Table | Time-Based Analysis |
| 📁 PBIX | Power BI Project File |
| 📷 PNG | Dashboard Preview Images |

## 📂 Data Model
The solution is built using four core business entities:
### Orders
Contains delivery transaction details including:
- Order ID
- Order Date
- Actual Delivery Date
- Order Status
- Delivery Time
- Hub Processing Time
- Delay Reason
- Driver Information
- Vehicle Information
- Customer Satisfaction Score
### Hubs
Contains hub-related operational information:
- Hub ID
- Hub Name
- Hub Capacity
### Drivers
Contains workforce information:
- Driver ID
- Driver Name
- Hire Date
- Experience Years
- Employment Type
- Performance Rating
### Vehicles
Contains fleet management information:
- Vehicle ID
- Vehicle Model
- Vehicle Status
- Purchase Date
- Breakdown Count
- Maintenance Information
### 🔍 Data Preparation & Validation
Before dashboard development, a complete data quality assessment was performed.I checked the data to make sure it was complete and ready for analysis. All tables (Orders, Hubs, Drivers, and Vehicles) were imported into Power BI, and I verified that all rows were loaded successfully. After importing the data, I reviewed the data type of each column and found that some date fields were not in the correct format. These columns were converted to the Date data type to support time-based analysis and reporting.

I then used Power Query's Column Quality and Column Distribution features to check for missing values, errors, and data issues. The results showed 0% errors and 0% empty values across the dataset. Since the data was already clean and consistent, no additional data cleaning was required. This ensured that the dataset was reliable and ready for data modeling, DAX calculations, and dashboard development.
### 🏗️ Data Modeling
After validating the data, I reviewed the relationships between all tables to ensure the data model was structured correctly. The dataset followed a star schema design, where the Orders table acted as the central fact table and the Hubs, Drivers, and Vehicles tables acted as dimension tables. This structure helps improve reporting performance and makes analysis easier.

While creating relationships, I noticed that the Orders table did not contain a Hub ID column. To connect the Orders and Hubs tables, I used the Hub Name column from both tables. A many-to-one relationship with single-direction filtering was created, which worked correctly for the reporting requirements. Relationships between Orders and Drivers, as well as Orders and Vehicles, were also verified to ensure accurate filtering and analysis across the dashboard. 

To support date-based analysis, I created a separate Date Table containing fields such as Date, Year, Month, Day, and Day of Week. The Date Table was then connected to the Orders table using the Order Date column. This allowed me to create time-based calculations and use DAX time intelligence functions for Month-over-Month (MoM) comparisons, trend analysis, and dynamic date filtering across the dashboard.

This data model allowed me to build the dashboard smoothly and create accurate calculations, filters, and visualizations across all pages.

## 📊 Dashboard Pages
### Dashboard 1: Executive Overview
#### KPI Metrics
##### Total Orders
- Current Month Orders
- Previous Month Orders
- MoM Growth %
##### On-Time Delivery Rate
- Current Month Performance
- Previous Month Performance
- MoM Change %
##### Customer Satisfaction (CSAT)
- Current Month CSAT
- Previous Month CSAT
- MoM Change %
##### Average Delivery Time
- Current Month Average
- Previous Month Average
- MoM Change %
#### Hub Insights
- Total Hubs
- Orders Processed vs Hub Capacity
- Hub Performance Ranking
#### Driver Insights
- Total Drivers
- Experience vs Performance Rating
- Drivers with Most Delays
#### Vehicle Insights
- Total Vehicles
- Active Vehicles
- Orders by Vehicle Model
### Dashboard 2: Hub Performance Overview
#### Visuals Included
- Total Number of Hubs (KPI)
- Orders Processed vs Hub Capacity
- Hub Performance Ranking
- Hub Processing Time Matrix
#### Business Value
Helps identify:
- Overloaded hubs
- Underutilized hubs
- Processing bottlenecks
- Capacity planning opportunities
### Dashboard 3: Driver Performance Overview
#### Visuals Included
- Number of Drivers
- Experience vs Rating Scatter Plot
- Drivers with Most Delays
- Driver Profile Summary
- Monthly Orders Trend
#### Driver Profile Details
- Hire Date
- Years of Experience
- Performance Rating
- Monthly Deliveries
#### Business Value
Supports:
- Performance evaluation
- Workforce planning
- Driver coaching
- Incentive programs
### Dashboard 4: Vehicle & Fleet Overview
#### Visuals Included
- Total Vehicles
- Active Vehicles
- Orders by Vehicle Model
- Vehicle Age vs Breakdown
- Breakdown by Vehicle Code
- Breakdown by Vehicle Model
- Orders by Vehicle Type
#### Business Value
Enables:
- Fleet utilization monitoring
- Breakdown analysis
- Maintenance planning
- Vehicle replacement decisions
## 🎨 User Experience Features
### Interactive Navigation
Custom navigation buttons were implemented to allow seamless movement between all dashboard pages.
#### Dynamic Filters
Users can analyze performance using:
- Year Filter
- Month Filter
- Driver Selection
- Vehicle Selection
- Hub Selection
#### Cross-Filtering
All visuals interact dynamically, enabling deeper operational analysis with minimal effort.
## 📈 Key Business Insights Delivered
### Operations Management
- Monitor delivery performance in real time.
- Track SLA compliance through on-time delivery rates.
### Hub Optimization
- Identify hubs operating beyond capacity.
- Improve resource allocation and processing efficiency.
### Driver Performance Analysis
- Detects high-performing and underperforming drivers.
- Evaluate the impact of experience on performance ratings.
### Fleet Management
- Monitor vehicle health and breakdown trends.
- Optimize fleet utilization and maintenance schedules.
### Customer Experience
- Track customer satisfaction trends.
- Understand the operational factors affecting customer feedback.
## 🚀 Project Outcome
This Power BI solution provides a complete operational visibility framework for logistics organizations. By integrating orders, hubs, drivers, and fleet data into a single analytical platform, decision-makers can proactively improve delivery efficiency, reduce operational bottlenecks, increase customer satisfaction, and optimize logistics performance across the entire network.
## Dashboard (Screenshot)
https://github.com/dr2546101/lOGISTICS-Dashboard/blob/main/SwiftRoute%20Logistics%20Dashboard.png

https://github.com/dr2546101/lOGISTICS-Dashboard/blob/main/Hubs%20Overview.png

https://github.com/dr2546101/lOGISTICS-Dashboard/blob/main/Vehicle%20Overview.png

https://github.com/dr2546101/lOGISTICS-Dashboard/blob/main/Drivers%20Overview.png









