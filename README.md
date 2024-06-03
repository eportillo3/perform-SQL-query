<h1>Perform a SQL query</h1>


<h2>Description</h2>
Use SELECT and FROM in SQL to return the information you need from a database. You’ll also use the ORDER BY keyword to sequence the information returned by a query based on a specified column.


<h2>Environments Used </h2>

- <b>MariaDB shell</b>

<h2>Scenario:</h2>

In this scenario, you have to determine which employee devices must be updated. You also need to investigate user login activity to explore if any unusual activity has occurred.

The information you need is located in the machines and login_attempts tables in the organization database.

Here’s how you’ll do this task: 

<b>First</b>, you’ll obtain information on the employee devices that must be updated. 

<b>Next</b>, you’ll examine the login attempts for unusual activity. 

<b>Finally</b>, you’ll use the ORDER BY keyword to sort the data returned by your SQL queries.


<h2>Tutorial walk-through:</h2>

<h3>Task 1. Retrieve employee device data</h3>

In this task, you need to obtain information on employee devices because your team needs to update them. The information you need is in the machines table in the organization database

<b>First</b>, you need to retrieve all the information about the employee devices.

1. Run the following query to select all device information from the machines table:

<img src="https://i.imgur.com/WuFfIsq.png" height="80%" width="80%"/>

The output returns all the contents of the machines table:

<img src="https://i.imgur.com/ZsSOhyI.png" height="80%" width="80%"/>
   
<b>Next</b>, you want to focus on the email client running on various devices.

2. Run the following query to select only the device_id and email_client columns from the machines table. Replace X with device_id and Y with email_client:

<img src="https://i.imgur.com/RxFTC5i.png" height="80%" width="80%"/>

<b>Now</b>, you need information on the operating systems used on various devices and their last patch date.

3. Complete the query to return only the device_id, operating_system, and OS_patch_date columns from the machines table. Replace X, Y, and Z with the columns that you need to return:

<img src="https://i.imgur.com/8vBFgos.png" height="80%" width="80%"/>


<h3>Task 2. Investigate login activity</h3>

In this task, you need to analyze the information from the log_in_attempts table to determine if any unusual activity has occurred.

<b>First</b>, you need to investigate the locations where login attempts were made to ensure that they’re in expected areas (the United States, Canada, or Mexico).

1. Write a SQL query to select the event_id and country columns from the log_in_attempts table.

<img src="https://i.imgur.com/sR1DDdv.png" height="80%" width="80%"/>

<b>Next</b>, you need to check if login attempts were made outside of the organization's working hours.

2. Write a SQL query that selects the username, login_date, and login_time columns from the log_in_attempts table.

<img src="https://i.imgur.com/XVWbPpU.png" height="80%" width="80%"/>

<b>Now</b>, you need to get a complete picture of all login attempts.

3. Write a SQL query that selects all columns from the log_in_attempts table, using a single symbol after the SELECT keyword.

<img src="https://i.imgur.com/7W2OzTW.png" height="80%" width="80%"/>


<h3>Task 3. Order login attempts data</h3>

In this task, you need to use the ORDER BY keyword. You'll sequence the data that your query returns according to the login date and time.

<b>First</b>, you need to sort the information by date.

1. Run the following query, which orders log_in_attempts data by login_date:

<img src="https://i.imgur.com/ukLF5kw.png" height="80%" width="80%"/>

<b>Now</b>, you need to further organize the previous results by ordering them by login_time.

2. Modify the query from the previous step by adding the login time to the ORDER BY clause. You must replace X with the appropriate column name:

<img src="https://i.imgur.com/kPMnv9U.png" height="80%" width="80%"/>



<h2>Conclusion</h2>

You have completed this activity, and you now have practical experience in running basic SQL queries to

- select specific columns from a table
- select all columns from a table by using an asterisk (*)
- sort query results using the ORDER BY keyword

  
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
