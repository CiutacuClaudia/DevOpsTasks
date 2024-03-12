# Task 3 : 

1. **Set Up MySQL Container:**
   - Run the following command to create a MySQL container:
     ```bash
     docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=<your_root_password> -p 3306:3306 -d mysql:latest
     ```
     Replace `<your_root_password>` with your desired root password.

2. **Create Database and Import Data:**
   - Access the MySQL container:
     ```bash
     docker exec -it mysql-container mysql -uroot -p<your_root_password>
     ```
   - Create the database named "company":
     ```sql
     CREATE DATABASE company;
     ```
   - Exit the MySQL prompt:
     ```sql
     exit;
     ```
   - Import the company.sql file into the "company" database:
     ```bash
     docker exec -i mysql-container mysql -uroot -p<your_root_password> company < /path/to/company.sql
     ```
     Replace `/path/to/company.sql` with the actual path to your `company.sql` file.

3. **Create User and Assign Permissions:**
   - Access the MySQL container:
     ```bash
     docker exec -it mysql-container mysql -uroot -p<your_root_password>
     ```
   - Create a user and grant all permissions for the "company" database:
     ```sql
     CREATE USER '<your_username>'@'%' IDENTIFIED BY '<your_password>';
     GRANT ALL PRIVILEGES ON company.* TO '<your_username>'@'%';
     FLUSH PRIVILEGES;
     ```
     Replace `<your_username>` and `<your_password>` with your desired username and password.

4. **Find Average Salary for Each Department:**
   - Access the MySQL container:
     ```bash
     docker exec -it mysql-container mysql -uroot -p<your_root_password>
     ```
   - Select the "company" database:
     ```sql
     USE company;
     ```
   - Run the SQL query to find the average salary for each department:
     ```sql
     SELECT d.department_name, AVG(e.salary) AS avg_salary
     FROM employees e
     JOIN departments d ON e.department = d.department_id
     GROUP BY d.department_name;
     ```