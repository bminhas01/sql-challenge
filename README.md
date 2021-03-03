# sql-challenge

This analysis studies information for employees at Pewlett Hackard. The dataset is comprised of six CSV files containing information for employees of the corporation from the 1980s and 1990s. The analysis requires designing tables to hold the data in the CSV files, inport the CSVs into a SQL database, and answer questions about the data. 

** Compiling the data

1. Inspect the CSVs and sketch out an ERD of the tables. Feel free to use a tool like [http://www.quickdatabasediagrams.com](http://www.quickdatabasediagrams.com).

2. Use the information you have to create a table schema for each of the six CSV files. Remember to specify data types, primary keys, foreign keys, and other constraints.
    * For the primary keys check to see if the column is unique, otherwise create a [composite key] (https://en.wikipedia.org/wiki/Compound_key). Which takes to primary keys in order to uniquely identify a row.
    * Create tables in the correct order to handle foreign keys.

3. Import each CSV file into the corresponding SQL table. **Note** be sure to import the data in the same order that the tables were created and account for the headers when importing to avoid errors.

** Analyzing the data

1. List the following details of each employee: employee number, last name, first name, sex, and salary.

2. List first name, last name, and hire date for employees who were hired in 1986.

3. List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.

4. List the department of each employee with the following information: employee number, last name, first name, and department name.

5. List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."

6. List all employees in the Sales department, including their employee number, last name, first name, and department name.

7. List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.

8. In descending order, list the frequency count of employee last names, i.e., how many employees share each last name.

** Bonus Analysis
1. Import the SQL database into Pandas. (Yes, you could read the CSVs directly in Pandas, but you are, after all, trying to prove your technical mettle.) This step may require some research. Feel free to use the code below to get started. Be sure to make any necessary modifications for your username, password, host, port, and database name:

   ```sql
   from sqlalchemy import create_engine

   engine = create_engine('postgresql://<PostgreSQL_username>:<PostgreSQL_password>@localhost:5432/<your_db_name>')
   
   connection = engine.connect()
   ```

   * Consult [SQLAlchemy documentation](https://docs.sqlalchemy.org/en/latest/core/engines.html#postgresql) for more information.

   * If using a password, do not upload your password to your GitHub repository. See the following for more information:
         - [https://www.youtube.com/watch?v=2uaTPmNvH0I]
         - (https://www.youtube.com/watch?v=2uaTPmNvH0I) 
         - [https://help.github.com/en/github/using-git/ignoring-files]         
         - (https://help.github.com/en/github/using-git/ignoring-files)

2. Create a histogram to visualize the most common salary ranges for employees.

3. Create a bar chart of average salary by title.
  * label the chart as appropriate
