# Example Queries for AdventureWorks and Travel Datasets

This file contains a collection of example queries for two different datasets: AdventureWorks and a travel dataset. These queries are designed to test various data retrieval and analysis functionalities.

## AdventureWorks Example Queries

### 1. Filter Questions (Finding Specific Records)

These queries test the system's ability to identify the correct column and value to pinpoint specific entries.

**Simple Single-Column Filter:**

*   "What is the email address for Ana Price?" (Tests FirstName and LastName filtering)
*   "Show me customer details for key 11000." (Tests numeric CustomerKey filtering)
*   "Find the order with order number SO45082." (Tests OrderNumber filtering from the sales file)

**Filter with a Condition:**

*   "List customers with the occupation 'Management'." (Tests filtering by Occupation)
*   "Display all orders for product key 310." (Tests numeric ProductKey filtering)

**Multi-Column Filter (More Advanced):**

*   "Is there an order from customer 11000 for product 344?" (Requires filtering on both CustomerKey AND ProductKey)
*   "Is there an order from customer 11001 for product 477?" (Requires filtering on both CustomerKey AND ProductKey)
*   "Show me orders placed by customer 12109 on February 1st, 2017." (Requires a three-part filter on CustomerKey, a specific OrderDate, and implicitly a ProductKey if not all products are desired)
*   "Show me orders placed by customer 12109 on January 14th, 2017." (Requires a three-part filter on CustomerKey, a specific OrderDate, and implicitly a ProductKey)

### 2. Sort Questions (Ranking by a Value)

These queries test the system's ability to identify the correct column to sort by and the correct direction (ascending/descending).

**Simple Ranking:**

*   "Who are the top 5 customers by annual income?" (Tests descending sort on AnnualIncome)
*   "Which 5 customers have the most children?" (Tests descending sort on TotalChildren)
*   "What are the 10 most recent orders?" (Tests descending sort on OrderDate)

**Ranking with "Lowest" or "Oldest":**

*   "What are the 5 lowest annual incomes?" (Tests ascending sort on AnnualIncome)
*   "Show me the 10 oldest customers." (Tests ascending sort on BirthDate)
*   "Which 10 orders had the smallest quantity?" (Tests ascending sort on OrderQuantity)

### 3. Count Questions (Measuring and Counting)

These queries test the system's ability to count rows, either in total or based on a specific filter.

**Total Count:**

*   "How many customers are in the file?" (Tests counting all rows in customers.csv)
*   "What is the total number of orders in 2017?" (Tests counting all rows in sales-2017.csv)

**Count with a Single Condition:**

*   "How many customers are homeowners?" (Tests counting after a filter on HomeOwner = 'Y')
*   "Count the number of customers who are single." (Tests counting after a filter on MaritalStatus = 'S')
*   "How many orders were for product 529 in 2017?" (Tests counting after a filter on ProductKey)

**Count with Negation:**

*   "How many customers are not homeowners?" (Tests counting after a filter on HomeOwner = 'N')
*   "How many customers do not have a prefix?" (A good test for handling null or empty values)

**Count with a Date Condition:**

*   "How many orders were placed in the year 2017?" (Tests counting after a filter on the year of OrderDate)

---

## Travel Dataset Example Queries

### 1. Filter Questions (Finding Specific Records)

These questions test the ability to find specific records based on one or more criteria.

**Simple Single-Column Filter:**

*   "What is the age of Wilma Mcinnis?" (Tests name filtering in users.csv)
*   "Show me the user details for code 15." (Tests numeric code filtering in users.csv)
*   "Find all flights operated by the 'Rainbow' agency." (Tests agency filtering in flights.csv)
*   "Show me all bookings for 'Hotel K'." (Tests name filtering in hotels.csv)

**Filter with a Condition:**

*   "List all users whose gender is 'none'." (Tests filtering by gender in users.csv)
*   "Display all flights from 'Brasilia (DF)'." (Tests filtering by from location in flights.csv)
*   "Find all hotel bookings in 'Salvador (BH)'." (Tests filtering by place in hotels.csv)

**Multi-Column Filter (More Advanced):**

*   "List all first-class flights from 'Brasilia (DF)' handled by 'FlyingDrops'." (Requires a three-part filter on flightType, from, and agency in flights.csv)

### 2. Sort Questions (Ranking by a Value)

These questions test the ability to sort the data to find top, bottom, oldest, or newest records.

**Simple Ranking:**

*   "Who are the top 5 oldest users?" (Tests descending sort on age in users.csv)
*   "What are the 5 most expensive flights?" (Tests descending sort on price in flights.csv)
*   "Which 5 hotel stays were the longest?" (Tests descending sort on days in hotels.csv)
*   "What are the 10 most recent hotel bookings?" (Tests descending sort on date in hotels.csv)

**Ranking with "Lowest" or "Oldest":**

*   "Which 10 flights have the shortest duration?" (Tests ascending sort on time in flights.csv)
*   "What are the 5 cheapest hotel stays by total cost?" (Tests ascending sort on total in hotels.csv)

### 3. Count Questions (Measuring and Counting)

These questions test the ability to count records, either in total or based on a specific condition.

**Total Count:**

*   "How many users are in the file?" (Tests counting all rows in users.csv)
*   "What is the total number of flights?" (Tests counting all rows in flights.csv)
*   "How many hotel bookings are there in total?" (Tests counting all rows in hotels.csv)

**Count with a Single Condition:**

*   "How many users are female?" (Tests counting after a filter on gender = 'female')
*   "Count the number of flights with the agency 'CloudFy'." (Tests counting after a filter on agency)
*   "How many hotel bookings were for 'Hotel BD'?" (Tests counting after a filter on hotel name)
*   "How many flights were 'economic' class?" (Tests counting after a filter on flightType)
