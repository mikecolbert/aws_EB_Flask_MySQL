# AWS - Using Elastic Beanstalk running a Python Flask website connected to MySQL
Assignment configuring a website using Elastic Beanstalk, Python Flask, and MySQL

#### Notes:

- The main python application file should be named *application.py*.
- The flask object name, defined in application.py should also be called *application*.
- Each route in your application should also contain the method. Probably *GET* and/or *POST*
- *.ebignore* contains the name of files we don't want pushed to the cloud.
- Use *pip freeze > requirements.txt* to create a requirements.txt file.
- Create a folder named *.ebextensions* which should contain:
  - A file named *python.config* that contains the commands to execute your application.
  - A file named environment_variables.config that contains any necessary environment variables.
- Zip .ebextensions, static, templates, .ebignore, application.py, requirements.txt
  - These six files should be at the root of the zip file. Not in a folder.
  - If you are using a Mac to zip your files, remove any extra, hidden files in the zip or you will get errors
  - ``` zip -d flask_app.zip __MACOSX/\* ```



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
Zip the 6 items necessary for the application - .ebextensions, static, templates, .ebignore, application.py, requirements.txt

### Step 6: Create an Elastic Beanstalk application
Upload the zip file.

### Step 7: Modify MySQL security group to give permission for EB application to access the database
Modify security groups.

### Step 8: Test the application
Visit the environment URL to prove the application works.

### Step 9: To Do
Figure out how to connect your domain to an EB application.
- https://medium.com/quick-code/setting-up-godaddy-domain-and-aws-route-53-with-elastic-beanstalk-within-15-minutes-a0276ff4ea6e
- https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-beanstalk-environment.html

Figure out how to set up a CodeDeploy Pipeline for an EB application.
- https://www.youtube.com/watch?v=b0g-FJ5Zbb8
