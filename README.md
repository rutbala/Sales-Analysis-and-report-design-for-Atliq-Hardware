# Sales Analysis and report design for Atliq Hardware

Part 1:
Here I have a Movies_db dataset with the following tables:

Movies

![3 1movies_db Index Match](https://github.com/user-attachments/assets/ec936e95-b508-4a61-a1e1-c59fecd29444)

Financials

![273764535-5945a590-1aa7-4d53-af10-6758cc816c8a](https://github.com/user-attachments/assets/e628c54d-ecba-4154-9789-b4f7c7954a2f)

I have used

VLOOKUP

![3 1movies_db VLOOKUP](https://github.com/user-attachments/assets/c2efe794-1184-4866-8dff-80d78b8a7223)

INDEX - MATCH 

![3 1movies_db Index Match](https://github.com/user-attachments/assets/ad94d265-7b91-49c3-b456-857d6531e087)

and XLOOKUP to bring data from Financials to match corresponding data in Movies Table.

![3 1movies_db XLOOKUP](https://github.com/user-attachments/assets/7aa3e641-26a9-4f58-bb10-3c37a41a8c8f)

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
