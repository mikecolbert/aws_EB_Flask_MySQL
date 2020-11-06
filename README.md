# aws_EB_Flask_MySQL
Assignment configuring a website using Elastic Beanstalk, Python Flask, and MySQL


### Step 1: Create a MySQL RDBMS
Create a MySQL with public access. Put it in the default VPC.

### Step 2: Edit MySQL security group to allow your computer access
Your IP address should be able to connect on port 3306.

### Step 3: Install MySQL Workbench
Install MySQL Workbench and connect to your database.

### Step 4: Create database users, tables, and data
Populate MySQL.

### Step 5: Edit Flask application
Edit .ebextensions/environment_variables.config to set database username, password, and hostname.
Zip the 6 items necessary for the application.

### Step 6: Create an Elastic Beanstalk application
Upload the zip file.

### Step 7: Modify MySQL security group to give permission for EB application to access the database
Modify security groups.

### Step 8: Test the application
Visit the environment URL to prove the application works.

### Step 9: To Do
Figure out how to connect your domain to an EB application
