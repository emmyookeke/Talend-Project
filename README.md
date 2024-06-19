
# Talend Data Integration
# Create an ETL job to read the data of employee, which is in the following format-
	Employee.csv
The output data should be stored in MSSQL database table.

To start the ETL process for the employee data, we first established a connection with the MSSQL database. We configured the database credentials, including the server address, database name, username, and password. This secure and reliable connection is crucial for us to smoothly transfer data from the source file into the target MSSQL database table, allowing us to effectively manage and analyze the data. Attached below are screenshots of our workspace that illustrate this process.

 
Create an ETL job to read the data of “Covid19 data.csv” and store it into the MSSQL database table.

In this ETL task, we focused on handling the "Covid19 data.csv" file. This involved similar preliminary steps where we ensured our MSSQL database connection was still active and secure. We then developed a specific ETL script to read the Covid19 data efficiently, mapping the relevant columns to the corresponding fields in our MSSQL database table. We tested the process to ensure accuracy and completeness of the data transfer. We have included screenshots of the scripts and database mappings below.

  
# Create an ETL job to read the data from the following JSON file and stored it into the CSV file
	Store.json

In tackling the JSON data from "Store.json," our team crafted an ETL job designed to extract data efficiently from the JSON format and then store it into a CSV file. We carefully parsed the JSON file, extracting relevant fields while maintaining data integrity and structure. After the extraction, we transformed the data to fit the CSV format specifications, ensuring each field was correctly aligned and formatted. Finally, we wrote the transformed data to a CSV file, preparing it for any further processing or analysis that might be needed. Below are the screenshots of the transformation logic and final CSV output, showcasing our detailed approach.

 
 
# Create an ETL job to read the data from the following XML file and store it into excel file-
	Book.xml

Our final ETL job involved processing data from "Book.xml," an XML file containing book information. We developed a procedure to read and extract data from this XML format, focusing on capturing all essential elements and attributes efficiently. After parsing the XML data, we transformed it to match the structure required by an Excel file, ensuring that the data alignment and format adhered to Excel standards. The processed data was then loaded into an Excel spreadsheet, creating a user-friendly and accessible format for data review and reporting. Below, we have attached screenshots demonstrating the XML to Excel conversion process and the final Excel output.
 

# Create an ETL job to read the data from following MSSQL table to Excel file.
	DimCustomer

For our fifth ETL task, we shifted focus to exporting data from the "DimCustomer" MSSQL table into an Excel file. We started by confirming our database connection settings to ensure seamless data access. Then, we implemented an ETL script tailored for exporting SQL table data. 

This script efficiently queried the "DimCustomer" table, extracting all necessary customer details. The data was then transformed to align with Excel's formatting requirements, including column headers and data types appropriate for Excel analysis. 

The data was loaded into an Excel file, providing a convenient format for further data manipulation or distribution. Screenshots of our Excel export process and the resulting file are attached below to illustrate our methods and outcomes.

 
 
# Create an ETL job to load the data from three different files as shown below and join these three different files based on the key columns (DeptId, AddrID). The output will store it into the CSV file call Employee.csv.
	EmpAddr.txt
	EmpDept.csv
	Employee.xlsx

Our sixth ETL task involved integrating data from three different sources: "EmpAddr.txt," "EmpDept.csv," and "Employee.xlsx." The key to this task was effectively joining these files based on shared columns, specifically 'DeptId' and 'AddrID'. 
We first read data from each file, ensuring we captured all necessary details while maintaining data integrity. After loading the individual datasets, we used an ETL tool to perform the join operation, aligning data across the three sources based on the specified key columns. 
We transformed the consolidated data to a uniform format suitable for a CSV file and then exported the unified dataset to "Employee.csv," ensuring the result was well-organized and accessible for any subsequent processing or analysis. Below are screenshots depicting the data joining process and a snippet of the final CSV output.

  
# Create an ETL job to load the data from “Product.xlsx” file having data for Product and Order, join them based on the key columns (ProductID). The output will store it into the MySQL database table call Sales. [Use join to join this table]

In our seventh ETL task, we focused on processing and integrating data from the "Product.xlsx" file, which contained separate sheets for Product and Order information. The crucial part of this task was to join these two datasets based on the 'ProductID' key column. 
First, we extracted both Product and Order data from the respective sheets within the Excel file, ensuring each dataset was accurately captured. We then implemented a join operation to merge these two datasets on 'ProductID', which allowed us to create a comprehensive view that combines product details with order specifics. After the join, we transformed the integrated dataset to align with the MySQL database's schema requirements and loaded the final joined data into a new MySQL table named 'Sales'. 
This step ensured the data was ready for querying and analysis in the database environment. Attached below are screenshots of our data processing steps and the schema of the 'Sales' table in MySQL, illustrating our methodical approach to data integration and storage.

 

# Create an ETL job to load from “ActiveEmployee.xlsx” file, load the data into the MSSQL database table based on the following conditions-
	Split the data into three different files based on the conditions-
o	If the salary <= 250000 then call it LowRange
o	If the salary > 250000 and salary <= 500000 then call it MediumRange
o	If the salary > 500000 then call it HighRange
	Combine the first name and last name of the employee and call it EmployeeName
	Calculate the age of the individual employee and call it Age column (int data type)
	Evaluate if Gender="M” then “Male” and if Gender= “F” then “Female”, call it Gender.
	Evaluate if Country Code="CAN” then “Canada”, if Country Code=”CHN” then “China” and so on, call this as a Country.
	Evaluate if Length of zipcode=4 then add two “00” as the beginning of the data, if Length of zipcode=5 then add a “0” as the beginning of the data and so on, make this column’s each data as 6. Ex- (1890 then 001890)

For our eighth ETL task, we managed data transformation and loading from the "ActiveEmployee.xlsx" file into the MSSQL database, with several conditional transformations and data splitting based on salary ranges. Initially, we loaded the data and immediately performed transformations including the concatenation of first and last names into a new 'EmployeeName' column, calculating each employee's age for the 'Age' column, and standardizing gender and country representations based on given codes.

To further refine our data, we split the dataset into three separate groups based on salary: 'LowRange' for salaries less than or equal to 250,000, 'MediumRange' for salaries between 250,001 and 500,000, and 'HighRange' for salaries over 500,000. Each group was then processed separately to apply unique naming conventions and transformations tailored to its range.

We modified the zipcode data to ensure a standard length of six characters by prefixing zeros 
where necessary, enhancing uniformity and readability. Once all transformations were applied, the datasets for each salary range were loaded into corresponding tables in the MSSQL database. Below, you'll find screenshots demonstrating our ETL processes, including data splitting, transformation logic, and the final structured data in the database.

# Create an ETL job to read the file with the following conditions and load into the MSSQL database table.
	Check the condition, if is present in the folder or not.
	If the file is present in the folder then only processed the file, else stop the job.
	Whenever there is a new file then insert and if there is an existing file which you have already processed then update.

Our ninth ETL task involves handling file processing with conditional checks and data loading into an MSSQL database. Initially, we implemented a file presence check to ensure that the process only proceeds if the required file exists in the specified folder. If the file is not present, the ETL job is designed to halt immediately, preventing any further execution.

To efficiently manage file changes, we utilize file timestamps or checksums to detect modifications or new files, triggering the appropriate insert or update actions. Attached below are screenshots illustrating the file checking mechanism, and the conditional logic used for inserting or updating data in the database.

 
# Create an ETL job Achieve all the files (in .zip format) from a directory.


For our tenth ETL task, we focused on archiving files from a specific directory into a .zip format. This process begins by scanning the designated directory to identify all files that need to be archived. Once identified, each file is programmatically compressed into a .zip archive using a scripted approach, which ensures that all files are securely stored and that the archive's integrity is maintained.
After the files are successfully archived, the original files can be optionally deleted or marked as archived based on the system's configuration to prevent reprocessing of the same files.
Below, are screenshots of the archiving process, along with the script used to compress the files into .zip format. 

 
 
# Create an ETL job to declare the number starting from 101 to 105, capture the value of each iteration. Use a flat file to capture the output. [tForLoop]

In our eleventh ETL task, we designed a job to iterate through a set range of numbers, specifically from 101 to 105, and capture the value of each iteration in a flat file. This task was executed using a 'tForLoop' component in our ETL tool, which allows for easy configuration of start and end values of the loop.
The process starts by initializing the loop at 101 and incrementing through to 105. During each iteration of the loop, the current number is captured and written directly to a flat file. This is achieved through a connected component that handles file writing operations, ensuring that each number is appended to the flat file in a new line.
we implemented error handling to manage any issues that might arise during the file writing process, such as file access permissions or disk space limitations. This ensures that the ETL job runs smoothly and efficiently, without data loss.
Below are screenshots of the ETL configuration, including the setup of the 'tForLoop' and the file output component. These images highlight how each part of the process is managed and showcase the resulting flat file containing the sequence of numbers from 101 to 105.

 

# Create an ETL job to read the data of “Financial Sample.xlsx” sort the data by (UnitsSold and SalePrice) columns and store it into a MSSQL Database table.

In our twelfth ETL task, we concentrated on processing financial data from the "Financial Sample.xlsx" file by sorting and then storing it into an MSSQL database table. This task involved several critical steps:
We began by reading the data from the "Financial Sample.xlsx" file using an Excel input component within our ETL tool. This allowed us to pull all necessary columns directly into 	our data flow.
Once the data was loaded into our ETL pipeline, we applied a sorting transformation. We configured the sorting component to organize the data first by 'UnitsSold' and then by 'SalePrice' in ascending order. This dual-column sorting ensured that our data was 	ordered based on primary and secondary criteria, facilitating more structured analysis downstream.
After sorting, the data was ready to be loaded into the designated MSSQL database table. We used a database output component to establish a connection to our MSSQL server and specified the target table where the data should be inserted.
Throughout the process, we ensured that data types and formats matched those required by the MSSQL table schema. Additionally, we implemented robust error handling to manage any issues related to data integrity or connection failures, ensuring a smooth and reliable data transfer.
After the ETL job was executed, we verified the data in the MSSQL database to ensure that it was correctly sorted and stored. We also maintained logs of the ETL process, which provided a detailed record of the operations performed and any issues encountered.
Below are screenshots of our ETL tool configuration showing the data flow, including the sorting and loading components, as well as a snippet of the sorted data in the MSSQL database. 

 
