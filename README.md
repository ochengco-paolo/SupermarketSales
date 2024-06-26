# Supermarket Sales
### Concept Idea
The project focuses on utilizing visualizations to convey a narrative based on supermarket sales data. Various graph types, such as bar graphs, are employed to enhance accessibility and understanding. It aims to analyze the information depicted in the charts to identify areas of strength and improvement for the supermarket. Through this analysis, they seek to generate smart ideas for boosting sales and enhancing customer satisfaction. The project's overarching goal is to transform data into visual stories that offer valuable insights, uncover patterns, and highlight trends to inform decision-making and ultimately improve the supermarket's overall performance.

### Data Source
https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales

### Data Exploration
The dataset comprises 1000 rows and includes columns such as Invoice ID, Branch City, Customer Type, Gender, Product Line, Unit Price, Quantity, Tax 5%, Total, Date, Time, Payment, COGS (Cost of Goods Sold), Gross Margin Percentage, Gross Income, and Rating

The data type in the "Date" column is inconsistent; some dates are in the date data type, while others are not.
![Screenshot 2024-03-31 112832](https://github.com/ochengco-paolo/SupermarketSales/assets/140794262/0ac0a5d4-0b87-4d5b-ac61-4095e6b6f104)

### Data Processing
After recognizing inconsistencies in the "Date" column format, I initiated a series of steps to standardize it to the format dd/mm/yyyy. Initially, I executed the **Text to Columns** function, utilizing the delimiter '/' to split the dates into separate columns for Day, Month, and Year.

![1](https://github.com/ochengco-paolo/SupermarketSales/assets/140794262/4d814b5b-ebeb-49ce-9189-dd4013c9dbec)

Following this split, I named the columns appropriately as "Day", "Month", and "Year" for clarity and ease of reference. Subsequently, to identify and address inconsistencies in the dataset, I applied conditional formatting to the "Month" column, highlighting cells where the value greater than 12.

Upon identification of inconsistent date formats, I filtered the dataset to isolate entries where the month value exceeded 12. Subsequently, I transferred these values to the "Day" column, recognizing them as potentially misplaced day values. Similarly, I transferred other day values to the "Month" column.

To differentiate these modified columns, I labeled them as "NewDay" and "NewMonth". Additionally, I introduced a new column labeled "NewDate" to represent the corrected date values. Utilizing the formula "=DATE(Year, Month, Day)", I generated the final output for the "Date" column.

![3](https://github.com/ochengco-paolo/SupermarketSales/assets/140794262/78b16f45-84c9-4c8d-95aa-d36f992c7bf1)

Following verification of the corrected date values, I removed the auxiliary columns "NewDay", "NewMonth", and "Year", streamlining the dataset. Finally, I renamed the "NewDate" column to "Date", ensuring consistency and clarity in column naming conventions.

![4](https://github.com/ochengco-paolo/SupermarketSales/assets/140794262/de04ca4e-f360-4be0-847a-e171755ab8d5)


### Data Visualization
The dashboard showcases the Supermarket Sales data for the year 2019, providing insights into sales performance, trends, and key metrics for analysis and decision-making.

![Supermarket Sales 2019](https://github.com/ochengco-paolo/SupermarketSales/assets/140794262/976a7efd-15d4-4843-8f15-fed00bef9ba7)

Access for my visualization:
https://public.tableau.com/app/profile/jhon.paolo.ochengco/viz/TermProject_17019389403540/Dashboard1?publish=yes&fbclid=IwAR0JuhRWUyJ5UfBpLXStOKzCDFuQDZWyAyb9jp8F4wohV9Zl0G8EF6nevzQ

### Insights
- Total Gross Income for the supermarket sales dataset shows that the overall income generated is15.38K. This means that, in total, the supermarket made that amount of money from all its sales.Understanding the total gross income is crucial for assessing the supermarket's financial performance.
- The Profit Margin Analysis graph for the supermarket's Product Lines shows which categories make the most money. Fashion Accessories have the highest profit margin at 8.476, meaning they bring in the most profit. Electronic Accessories and Food and Beverages also do well. But Health and Beauty make the least profit, with a margin of 7.238, so there's room for improvement there. This info helps the supermarket make smart choices, like focusing on products that make more money and adjusting prices if needed. Keeping an eye on costs, what customers like, and checking the profits regularly will help the supermarket stay successful in the long run.
- The pie chart shows almost equal numbers of Normal and Member customers: 499 normal and 501 members. This balance suggests a good mix of occasional and regular shoppers. With more Members, the supermarket can offer special deals to keep them loyal. It's important to understand both groups' preferences for tailored marketing and customer satisfaction. By improving the membership program and listening to feedback, the supermarket can foster a sense of community and ensure future success.

