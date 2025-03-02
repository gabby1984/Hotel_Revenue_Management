Hotel Revenue Management Dashboard

📌 Project Overview

• This project analyzes hotel revenue trends using Power BI, focusing on customer segmentation, seasonal trends,   and agent performance from 2018 to 2020. The goal is to provide actionable insights for optimizing hotel revenue strategies.

📊 Tools Used

• Power BI (Data Modeling, DAX, M Query)

• Microsoft Excel (Data Cleaning, Transformation)

📁 Dataset

• Hotel Revenue Task.xlsx: Booking data from 2018 to 2020

• Data Dictionary.xlsx: Explanation of key dataset fields

• Calendar Table.txt: Custom date table for time analysis


🛠️ Data Preparation for Visualization

• This section outlines the steps taken to import, clean, transform, and prepare the data before creating visualizations.

1. Importing Data

• Open Power BI Desktop.
• Click on Blank Report.
• Navigate to the Home Tab.
• Click on the drop-down beside Get Data.
• Select Excel Workbook (since the dataset is in Excel format).
• Locate the saved dataset, select it, and click Open.
• Check the boxes for the required tables within the workbook.
• Click on Transform Data to open the Power Query Editor.

2. Cleaning and Transforming Data

 2.1 Preparing the Hotel Revenue Data

Note: The workbook contains hotel revenue data for 2018, 2019, and 2020, along with Market Segment and Meal Cost data.
• Ensure column labels across the datasets match:
• Rename the column 'adr' in 2019 and 2020 datasets to 'AVG Daily Rate' (to match 2018).
• Append 2019 and 2020 datasets to the 2018 dataset: Navigate to the Home Tab > Append Queries drop-down > Append   Queries as New.
• Select Three or more tables.
• Add 2019 and 2020 datasets.
• Click OK.
• Rename the new dataset to a meaningful name.
• Verify and update data types for consistency:'is_canceled', 'is_repeated_guest', and 'Agent' → Text.
   'AVG Daily Rate' → Fixed Decimal Number.

 2.2 Cleaning the Market Segment Data

• Remove the first row: Home Tab > Reduce Rows > Remove Rows > Remove Top Rows.
• Enter 1 in the number of rows field and click OK.
• Promote the first row as headers: Home Tab > Transform > Use First Row as Headers.
• Change the 'Discount' column data type to Percentage (%).

 2.3 Cleaning the Meal Cost Data

• Remove the first row and promote the first row as headers (same steps as above).
• Change the 'Cost' column data type to Fixed Decimal Number.

3. Creating the Date Table
• Click on New Source > Text/CSV.
• Locate and select the Calendar table file.
• Click Open, then OK.
• Open the Advanced Editor from the Home Tab:
• Delete the default content.
• Paste the given content of the calendar table.
• Click Done.
• Set the date parameters:
    StartDate: 1/1/2018
    EndDate: 12/31/2020
    FYStartMonthNum (optional): 1
    WDStartNum (optional): 1
• Click Invoke.
• Rename the table to Date Table.
• Convert month names to numeric equivalents.
• Merge date-related columns: Select Day, Month, and Year columns. Transform Tab > Merge Columns.
• Set separator as /.
• Rename the merged column to Date.
• Change data type to Date.

4. Finalizing Data Preparation
• Disable loading for individual 2018, 2019, and 2020 datasets: Right-click on each dataset and disable load.
• Apply all transformations: Click Close & Apply.

• The dataset is now cleaned, transformed, and ready for visualization in Power BI.

🔍 Key Features of the Dashboard

Page 1 – Revenue Insights

📌 KPIs Displayed: Total Revenue, Total Stay Length, Repeat Guests, Total Cancellations, Total Bookings, and Average Daily Rate (ADR).

Revenue Breakdown by Customer Type (Bar Chart)

Revenue Trends Over Time (Line Chart with Monthly Analysis)

Revenue by Hotel Type and Year (Clustered Bar Chart)

Reservation Status Breakdown (Pie Chart)

Market Segment Performance (Stacked Bar Chart)

Page 2 – Customer & Agent Insights

📌 KPIs: Stay Length by Season, Festive Days, Agent Performance.

Stay Length Analysis (Weekday vs. Weekend) (Pie Chart)

Customer Stay Length During Festive Days (Doughnut Chart)

Stay Length by Season (Bar Chart)

Top 5 Performing Agents (Bar Chart)

Least Performing Agents (Table)

Page 3 – Summary & Definitions

📌 Key Definitions: Seasons
📌 Top Insights:
✔️ Transient customers generated the highest revenue.
✔️ August 2019 had the highest monthly revenue.
✔️ City hotels outperformed resort hotels in 2019 & 2020.
✔️ Online TA (Travel Agent) was the highest revenue-generating segment in 2019 & 2020.
✔️ Agent 9 had the highest total stay length.
✔️ Guests stayed longer on weekdays than weekends.
✔️ Summer saw the highest total stay length; winter had the lowest. 
    
📌 GitHub Repository Structure

📂 Hotel_Revenue_Management
│── 📁 Data & Instructions  # Dataset & Documentation
│── 📁 PowerBI_Dashboard  # Power BI File (.pbix)
│── 📁 Visualizations  # Screenshots of Dashboards
│── README.md  # Project Documentation
