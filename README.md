

#SALES DATA ANALYSIS DASHBOARD

DASHBOARD LINK: https://drive.google.com/file/d/1WfizxLmC5Xgq4Q3dMA8kkYEL_0YlNprb/view?usp=sharing

#PROBLEM STATEMENT 
In today's competitive retail landscape, understanding sales trends, identifying top-performing products, and optimizing revenue metrics are critical for making informed business decisions. However, with a large and complex sales dataset, it becomes challenging to extract actionable insights without the right tools and techniques. My objective is to analyze the sales data to uncover trends over time, determine the best-selling products, calculate essential revenue metrics, and create a visually engaging and interactive dashboard. This analysis will empower the business to enhance its sales strategies, optimize inventory management, and drive overall profitability.


# Description
In this project, I dove into a large sales dataset to extract valuable insights. I explored sales trends over time, identified the best-selling products, calculated revenue metrics such as total sales and profit margins, and created visualizations to present these findings. This project showcased my ability to manipulate and derive insights from large datasets, enabling me to make data-driven recommendations for optimizing sales strategies.

# Column Description for Sales Data Analysis
- Order ID
- Product
- Quantity Ordered
- Price Each
- Order Date
- Purchase Address
- Month
- Sales
- City
- Hour

# Steps Followed 
1. Data Transformation:
1. Promoting Headers: I used the "Use First Row as Headers" function in Power BI to set the first row as column headers.
2. Detecting Data Types: Navigated to the "Transform Data" tab and selected "Detect Data Type" to automatically assign the appropriate data types to each column.
3. Splitting Date and Time: Split the datetime column into separate date and time columns using the "Split Column" option with a space delimiter. After these transformations, I clicked "Close and Apply" to save the changes.

![Data Manipulation Steps](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/97a436bc-1cee-4955-9154-39517178407e)


2. Visualization Process:
1. Sales Trend Over Time (Line Chart):
   - Why this visualization: The line chart is perfect for showing trends over time, highlighting peaks and troughs in sales.
   - Process: To visualize sales trends over time, I selected the "Month" column, navigated to "Column Tools," and chose "Sort Column" to sort by month number. Then, I used a line chart to display the sales trend, making it easy to see how sales evolved throughout the year.

   ![Monthly Sales](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/ce800b5a-7637-4765-b235-e7927d2216fc)

   
2. Best-Selling Products by Sales Count (Tree Map):
   - Why this visualization: The tree map is ideal for showing proportions and making it easy to identify top-selling products.
   - Process: For identifying the best-selling products, I used a tree map. I dragged the "Product" column to the "Category" field and the "Sales" column to the "Value" field. To focus on the top 5 products, I used the "Top N" filter method and customized the visualization with the "Format" function.

![Top 5 Best-Selling Products](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/8b4af179-dd8d-42c8-a536-2d1326597617)

   
3. Top 5 Best-Selling Products Stacked Bar Chart):
   - Why this visualization: The stacked bar chart is effective for comparing quantities across categories, clearly displaying the best-selling products.
   - Process: Created a stacked bar chart by dragging the "Product" column to the Y-axis and the "Quantity Ordered" column to the X-axis. Applied the "Top N" filter to highlight the top 5 best-selling products.
   
4. Top 5 Cities by Sales (Funnel Chart):
   - Why this visualization: While a map would have been more intuitive for geographical data, the funnel chart still allowed for easy comparison of sales across cities.
   - Process: Due to the lack of access to map visualizations, I opted for a funnel chart to display the top 5 cities by sales. I dragged the "City" column to the "Category" field and the "Sales" column to the "Values" field, then used the "Top N" filter to identify the top cities. This visualization, while unconventional, effectively communicated the data.

![Top 5 Cities by sales](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/d5d80547-3b5e-4643-b231-6273b5156fb3)

   
5. Weekly Sales Distribution (Column Chart):
   - Why this visualization: The column chart is excellent for displaying distribution across categories, such as days of the week, to identify patterns.
   - Process: To analyze sales distribution throughout the week, I created a new "Weekdays" column by duplicating the date column and transforming it to show the names of the week. This column was added to the X-axis of a column chart, with "Sales" on the Y-axis. This helped identify which days of the week had the highest sales, guiding inventory management and staffing decisions.

![Weekly Sales](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/432d94db-9fbc-4fff-9ac5-b678050a4b06)

   
6. Interactive Dashboard with Slicers:
   - Why this visualization: Slicers enhance interactivity, allowing users to filter and explore the data dynamically.
   - Process: To make the dashboard interactive, I added slicers for Month, Weekdays, City, and Product. By dragging the relevant columns into the slicer options and configuring the layout, users can easily filter and explore the data.

![Weekdays Slicer](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/6900eeda-2d87-4e22-972a-80ebf3001f67)
![City and Month Slicer](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/2a4a2114-fb57-4b35-859d-ced3c5be6d59)
![Product Slicer](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/fe37f6f9-5cff-46ea-93bc-596b02ac8538)

   
7. Revenue Metrics (Card Visualization):
   - Why this visualization: The card visualization is best for highlighting single metrics like total sales and profit margins, providing a quick overview of key performance indicators.
   - Process: To display key revenue metrics, I used card visualizations:
     - Total Profit: Calculated by dragging the "Sales" column into a card and renaming it to Revenue. Adjusted the display units to millions and set the decimal places to 2.

![Total Revenue](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/a42058b6-073c-4e8e-822d-a3e3b7774d59)

     - Sales Quantity: Calculated by summing the "Quantity Ordered" column and displaying it in a card.

![Sales Qty](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/43ac6e71-95ea-46eb-94f9-96badf58682b)

     - Profit Margin: Created a new measure for total cost (sum of "Price Each") and total sales (sum of "Sales").
# Process;
 1. Clicked on new measure 
 2. Find the total cost and the total sales by using the new measure. Formula for both follows respectively; 

Total Cost = sum('Sales Data'[price each])
Total Sales = sum('Sales Data'[sales])

 3. The profit margin was calculated using the formula:
       
       Profit Margin = ([Total Sales] - [Total Cost]) / [Total Sales] * 100
       
       Displayed this measure in a card and customized its appearance.


![Profit Margin](https://github.com/stellapy/Sale_Data_Analysis/assets/153457347/6f865fbe-38cb-4b1d-a5d3-8de3dce17dfb)

# Explanation of Visualization Choices
- Line Chart: Perfect for showing trends over time, highlighting peaks and troughs in sales.
- *Tree Map:* Ideal for showing proportions and making it easy to identify top-selling products.
- Stacked Bar Chart: Effective for comparing quantities across categories, clearly displaying the best-selling products.
- Funnel Chart: While a map would have been more intuitive for geographical data, the funnel chart still allowed for easy comparison of sales across cities.
- Column Chart: Excellent for displaying distribution across categories, such as days of the week, to identify patterns.
- Card Visualization: Best for highlighting single metrics like total sales and profit margins, providing a quick overview of key performance indicators.

Dashboard Design
A well-designed dashboard includes images and visual elements to enhance user engagement and understanding. In my dashboard, visualizations are chosen to communicate specific insights effectively, ensuring that the data tells a compelling story.

I hope this project showcases not only my technical skills in data analysis and visualization but also my ability to present data in a clear, engaging, and actionable way. If you have any questions or feedback, I'd love to hear them.
