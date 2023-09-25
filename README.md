# sqlite_database_operations
Homework 3 for HHA 504


The first dataset is information from St Josephs and the second dataset is from New York Presbyterian.

The first dataset includes Billing/Charge Code, Charge Description, Rev Code, CPT/HCPC, price, NDC, variable and value. 

The second dataset includes information about Codes(CPT/DRG), descriptions, Rev Code, Gross Charges, Discounted Cash Price, variable and value.

In order to replicate this process you would need to create a temporary and locate database using sql lite. Create a variable conn that connects to sqlite and create a database named health. Then you put in c.execute and create a table with the columns you would like. Then you commit these using conn.commit(). From here, you execute and  do c.fetchall(). From here you can then inser the data into the table starting with sql_query. Then you again execute and commit. Then in another sql query you select all from the table and do c.execute(sql_query_2) and print(c.fetchall()). Then creame an engine to connect to the database created through sqlite. From here you can do pd.read_sql_query('select * from s;",conn). Then you load in your real data using pd.read and create a variable stjoseph_modified and set it equal to df.melt. From there do .describe and value_counts for the columns, and test that it was put in properly. 
