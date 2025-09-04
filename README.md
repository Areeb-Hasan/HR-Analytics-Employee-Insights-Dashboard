# HR-Analytics-Employee-Insights-Dashboard

This project is an end-to-end data analysis initiative for AtliQ Technologies, a real-world company, with the goal of providing actionable insights to their HR department. Using a real dataset, I transformed raw attendance data into a dynamic, interactive dashboard that helps stakeholders understand key employee metrics and make data-driven decisions. The final solution allows for monitoring crucial KPIs such as presence, sick leave, and work-from-home percentages.

Data Handling and Transformation:
A significant challenge in this project was combining data from multiple monthly attendance sheets into a single, cohesive dataset. Each month's data was stored in a separate worksheet within the same Excel file, and the columns were not consistently ordered, making a direct append difficult.

To overcome this, I leveraged Power Query to create a robust and automated data transformation process. The key steps were:

Connecting to the Data Source: I established a connection to the folder containing the Excel files, which automatically created a list of all files.

Creating a Custom Function: Instead of manually transforming each sheet, I built a custom function to process a single file. This function included steps to:

Navigate to the file's data.

Promote the first row to headers.

Clean and standardize column names.

Ensure all necessary columns were present and in the correct data type.

Invoking the Function: This function was then invoked across all files in the folder. This step was crucial for automating the process and ensuring data from all months was processed uniformly, regardless of inconsistencies in the original worksheets.

Appending the Queries: The results from all processed files were then combined into a single master table, ready for analysis.

This approach was heavily guided by a resourceful blog post that detailed a solution for combining multiple Excel worksheets: Power BI: Combine Multiple Excel Worksheets.

Business Questions Addressed
What is the overall employee presence percentage?

How does the sick leave percentage trend over time?

What is the distribution of work-from-home days by department?

Are there any patterns in attendance that could indicate operational issues?

Key Insights and Recommendations
The dashboard provides several key insights to help the HR team at AtliQ Technologies. For example, the analysis revealed a consistent drop in presence during certain months, which could be linked to holiday seasons. The sick leave percentage also showed a minor but consistent increase in the winter months. These insights allow the HR team to proactively manage workforce planning and implement policies that support employee well-being and productivity.

Technologies Used
Microsoft Power BI: Used for data modeling, transformation, and creating the final dashboard.

DAX (Data Analysis Expressions): Utilized to create calculated measures and columns for key metrics like presence and leave percentages.

Microsoft Excel: Source of the raw data files.
