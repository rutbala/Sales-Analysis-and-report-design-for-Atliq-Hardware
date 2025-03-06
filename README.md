# Sales-Analysis-and-report-design-for-Atliq-Hardware

Project Rundown:
▪ Data Source:
I had data in the form of multiple CSV files. These files held the keys to unlocking insights for Atliq hardware.

▪ Data Transformations:
Data transformation was a crucial part of this project. I had to clean, merge, and shape the data to make it ready for analysis. This step is like turning rough diamonds into sparkling gems, and it's where the magic begins.

▪ Creating a Date Table:
To ensure consistent time analysis, I crafted a date table using the date range from the data. Atliq's fiscal year runs from September to August, so I aligned all data with this fiscal calendar.

▪ DAX Formulas and Pivot Tables:
I flexed my DAX skills and put together some nifty pivot tables to generate a variety of insightful reports, including:

Customer Performance Report: Deep customer analysis that's pure gold for our sales strategies. image

Market Performance vs Target 2021: A deep dive into how we're performing against the targets set for 2021. image

Top 10 Products by Percentage Increase: Identifying those star products that saw impressive net sales growth from 2020 to 2021. image

Division Report: A snapshot of our net sales data for 2020 and 2021, complete with those all-important growth percentages. image

Product Quantity Report: Highlighting our best and worst performers in terms of quantity sold. image image

New Products in 2021: Spotting the newcomers we added to our lineup in 2021. image

Top 5 Countries by Net Sales: A peek into our global performance, showcasing the top players. image

User-Centric Design:
I'm all about making data user-friendly. So, I've displayed all numbers in an easily readable format and used conditional formatting to make the most important data pop.

Data integration and analysis are our compass for making informed, data-driven decisions. These reports are the secret sauce that will drive Atliq Hardware toward even greater success.

Part 3:
The objective: To use power pivot, data modeling, Dax, and pivot tables in Excel to create reports on hospitality data.
Data input: booking table and Properties table

The fact bookings file contains various columns including booking ID, property ID, check-in date, month, week number, booking platform, ratings given, booking status, successful bookings, and capacity. This file contains details about every booking made for a specific property or hotel.

Dimension properties file contains additional details about each property

Steps followed:
Load the data in an Excel file directly into the data model for data cleaning. Once the data cleaning is done, Use the "only create connections" option and "add this to the data model" to load data.

In the Power pivot data model, establish the relationship between both tables by connecting the property ID.

image

Create a pivot table from the data model option.

Generate DAX measures to calculate sum, count, and average functions.

image

The first report shows all the property performance for each Property: image image

The second report is booking platforms by week with filters for property name category and City. image image

key findings:
Revenue Leader for Business Category in June:
📈 I identified the property within the business category that generated the highest revenue in the month of June, showcasing the impact of data-driven decisions. image

July's Average Rating for 'Atliq Blu': 🌟 'Atliq Blu' received an average rating of 4.6 in the month of July.
This type of insight can help businesses understand their customer feedback better. image

Most Effective Booking Platform for 'Atliq Grands' (Week 'w27'): 🏨 For 'Atliq Grands' in the week of 'w27', I pinpointed the most effective booking platform in terms of revenue generation.
This kind of knowledge can boost future marketing strategies. image

Part 2:
The objective: To use Power Query for data cleaning and data transformation for the given datasets.
You have been given two CSV files to work with: bookings_data.csv rooms_data.csv

bookings_data: The bookings_data file consists of several columns, such as

date, property_id, property_name, hotel_type, city|city_code, room_id, successful_bookings, and capacity.

This file provides insights into the number of successful bookings made for a property on a given date and in a specific city, as well as the overall capacity of the property.

rooms_data: The rooms_data file consists of two columns,

room_id and room_class.

This file is useful in determining the room_class associated with each room_id in the bookings_data file.

Steps followed:

Open a new Excel file and load the two provided CSV files using the "From Text/CSV" option. Then, open Power Query.

Change the data type of the "property_id" column to "text".

Some values in the "property_name" column are shown as "Atliq bay" instead of "Atliq Bay". Replace these values to show "Atliq Bay" instead.

Format the "property_type" column by removing any unnecessary leading or trailing spaces using the TRIM() function.

The "city|city_code" column includes both the city and city_code separated by a '|' symbol. Split this column to separate these two entities and rename the resulting columns accordingly.

Create a new conditional column called "Availability Status". If "successful_bookings" equals "capacity", set the value to "sold out"; otherwise, set it to "vacant".

Create a new custom column called "occ%", which represents the ratio of successful_bookings to capacity. Change the data type to a percentage format.

Merge the two tables, "bookings_data" and "rooms_data", on the "room_id" column to add the "room_class" column to the "bookings_data" table. Reorder the columns so that "room_class" is next to "room_id".

Extract the month_name from the "date" column.

Part 1:
Here I have a Movies_db dataset with the following tables:

Movies

image

and Financials

image

I have used

VLOOKUP
image

INDEX - MATCH image

and XLOOKUP to bring data from Financials to match corresponding data in Movies Table.

image

About
Data analysis with Excel

Resources
 Readme
 Activity
Stars
 0 stars
Watchers
 1 watching
Forks
 1 fork
Report repository
Releases
No releases published
Packages
No packages published
Footer
© 2025 GitHub, Inc.
Footer navigation
Terms
Priva
