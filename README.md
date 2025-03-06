# Part 4:
# Sales Analysis and report design for Atliq Hardware

## Project Rundown:

### ▪ Data Source:
I had data in the form of multiple CSV files. These files held the keys to unlocking insights for Atliq hardware.
    
### ▪ Data Transformations:
Data transformation was a crucial part of this project. I had to clean, merge, and shape the data to make it ready for analysis. This step is like turning rough diamonds into sparkling gems, and it's where the magic begins.
    
### ▪ Creating a Date Table:
To ensure consistent time analysis, I crafted a date table using the date range from the data. Atliq's fiscal year runs from September to August, so I aligned all data with this fiscal calendar.
    
### ▪ DAX Formulas and Pivot Tables:
I flexed my DAX skills and put together some nifty pivot tables to generate a variety of insightful reports, including:

1. Customer Performance Report: Deep customer analysis that's pure gold for our sales strategies.
   ![image](https://github.com/mythilyram/Excel/assets/123518126/b5f30bb9-f76c-40f3-b97b-64d774c4d54c)


2. Market Performance vs Target 2021: A deep dive into how we're performing against the targets set for 2021.
![image](https://github.com/mythilyram/Excel/assets/123518126/42c5f4f7-b192-44d2-a650-2ff2336813df)

3. Top 10 Products by Percentage Increase: Identifying those star products that saw impressive net sales growth from 2020 to 2021.
![image](https://github.com/mythilyram/Excel/assets/123518126/0fa85919-6493-4ee7-91b8-fe3433c5ecb9)
	
4. Division Report: A snapshot of our net sales data for 2020 and 2021, complete with those all-important growth percentages.
![image](https://github.com/mythilyram/Excel/assets/123518126/712b6628-5d6b-4034-b012-6c998519073e)

5. Product Quantity Report: Highlighting our best and worst performers in terms of quantity sold.
![image](https://github.com/mythilyram/Excel/assets/123518126/c3ed3f48-77c3-4a66-b0f9-d2bb33283f5a)
![image](https://github.com/mythilyram/Excel/assets/123518126/b223aee6-09f2-424e-8d84-72ffe0d8856a)

6. New Products in 2021: Spotting the newcomers we added to our lineup in 2021.
![image](https://github.com/mythilyram/Excel/assets/123518126/e35bc181-a060-4290-9823-03d23f69ac7a)

7. Top 5 Countries by Net Sales: A peek into our global performance, showcasing the top players.
![image](https://github.com/mythilyram/Excel/assets/123518126/e7225189-c464-48b0-afe8-250aa83d6c7f)

# User-Centric Design: 
I'm all about making data user-friendly. So, I've displayed all numbers in an easily readable format and used conditional formatting to make the most important data pop.

Data integration and analysis are our compass for making informed, data-driven decisions. These reports are the secret sauce that will drive Atliq Hardware toward even greater success.

# Part 3:
 ### The objective: To use power pivot, data modeling, Dax, and pivot tables in Excel to create reports on hospitality data. 

Data input:
booking table and 
Properties table 

1. The fact bookings file contains various columns including booking ID, property ID, check-in date, month, week number, booking platform, ratings given, booking status, successful bookings, and capacity. This file contains details about every booking made for a specific property or hotel.

2. Dimension properties file contains additional details about each property

### Steps followed:

1. Load the data in an Excel file directly into the data model for data cleaning. Once the data cleaning is done, Use the "only create connections" option and "add this to the data model" to load data.

2. In the Power pivot data model, establish the relationship between both tables by connecting the property ID.
3. ![image](https://github.com/mythilyram/Excel/assets/123518126/f9f0e1f8-6a23-4770-9b16-5bdeae759b03)

4. Create a pivot table from the data model option.

5. Generate DAX measures to calculate sum, count, and average functions.
6. 
![image](https://github.com/mythilyram/Excel/assets/123518126/b754837c-ebb3-4fcf-80f6-557fd39b0351)

The first report shows all the property performance for each Property:
![image](https://github.com/mythilyram/Excel/assets/123518126/5464c0b6-9b88-480e-8bfe-cb682e6ab318)
![image](https://github.com/mythilyram/Excel/assets/123518126/4a3b7ab1-2349-4fa2-8aa3-858f198d15b8)


The second report is booking platforms by week with filters for property name category and City.
![image](https://github.com/mythilyram/Excel/assets/123518126/b38c1501-2284-44ce-9156-b386621a7df7)
![image](https://github.com/mythilyram/Excel/assets/123518126/4a30d430-deca-42f6-a669-2dff39bc1a38)

### key findings:
#### Revenue Leader for Business Category in June:
> 📈 I identified the property within the business category that generated the highest revenue in the month of June, showcasing the impact of data-driven decisions.
![image](https://github.com/mythilyram/Excel/assets/123518126/71cb04b5-89f0-4039-b994-ba7753eee16f)

#### July's Average Rating for 'Atliq Blu': 🌟 'Atliq Blu' received an average rating of 4.6 in the month of July.
> This type of insight can help businesses understand their customer feedback better.
![image](https://github.com/mythilyram/Excel/assets/123518126/8e788541-bac8-4de0-a0ab-e8d525b13de1)

#### Most Effective Booking Platform for 'Atliq Grands' (Week 'w27'): 🏨 For 'Atliq Grands' in the week of 'w27', I pinpointed the most effective booking platform in terms of revenue generation.
>This kind of knowledge can boost future marketing strategies.
![image](https://github.com/mythilyram/Excel/assets/123518126/e57c3d46-dcbc-4863-921a-994138ee6276)



# Part 2:
 ### The objective: To use Power Query for data cleaning and data transformation for the given datasets. 
 You have been given two CSV files to work with: 
	 bookings_data.csv
	 rooms_data.csv



1. bookings_data: The bookings_data file consists of several columns, such as
   >date, property_id, property_name, hotel_type, city|city_code, room_id, successful_bookings, and capacity.
   
   This file provides insights into the number of successful bookings made for a property on a given date and in a specific city, as well as the overall capacity of the property.



3. rooms_data: The rooms_data file consists of two columns,
   > room_id and room_class.
   
   This file is useful in determining the room_class associated with each room_id in the bookings_data file.

Steps followed:

1. Open a new Excel file and load the two provided CSV files using the "From Text/CSV" option. Then, open Power Query.

2. Change the data type of the "property_id" column to "text".

3. Some values in the "property_name" column are shown as "Atliq bay" instead of "Atliq Bay". Replace these values to show "Atliq Bay" instead.

4. Format the "property_type" column by removing any unnecessary leading or trailing spaces using the TRIM() function.

5. The "city|city_code" column includes both the city and city_code separated by a '|' symbol. Split this column to separate these two entities and rename the resulting columns accordingly.

6. Create a new conditional column called "Availability Status". If "successful_bookings" equals "capacity", set the value to "sold out"; otherwise, set it to "vacant".

7. Create a new custom column called "occ%", which represents the ratio of successful_bookings to capacity. Change the data type to a percentage format.

8. Merge the two tables, "bookings_data" and "rooms_data", on the "room_id" column to add the "room_class" column to the "bookings_data" table. Reorder the columns so that "room_class" is next to "room_id".

9. Extract the month_name from the "date" column.


# Part 1:

Here I have a Movies_db dataset with the following tables:

Movies

![image](https://github.com/mythilyram/Excel/assets/123518126/8395bf9a-4383-4fe8-8562-050b6da85f96)

and Financials

![image](https://github.com/mythilyram/Excel/assets/123518126/5945a590-1aa7-4d53-af10-6758cc816c8a)

I have used 
1. VLOOKUP

![image](https://github.com/mythilyram/Excel/assets/123518126/815dc622-42fd-43d5-974c-d295cd524f7b)


2.  INDEX - MATCH
![image](https://github.com/mythilyram/Excel/assets/123518126/2cbc3197-baf7-4e02-9fd3-eb4014ec79db)

3. and XLOOKUP to bring data from Financials to match corresponding data in Movies Table.

 ![image](https://github.com/mythilyram/Excel/assets/123518126/2f5155d8-ff46-4051-8b0b-5167e498e7e2)
