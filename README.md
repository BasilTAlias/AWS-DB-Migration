# Café Application Database Migration

This project demonstrates the process of migrating the database of a café application from a local EC2 instance to Amazon RDS. The project includes:

- Migrating the database from EC2 to RDS.
- Updating the application to use the new RDS endpoint.
- Stopping the EC2-based MariaDB database.
- Testing the application to ensure data is intact and the application is working with RDS.

## Technologies Used:
- AWS EC2
- AWS RDS
- PHP
- MariaDB
- AWS Secrets Manager

## Steps:
- Create an RDS database instance.
- Export data from a MariaDB database by using mysqldump.
- Connect an SQL client to an RDS database.
- Migrate data from a MariaDB database that runs on an EC2 instance to an RDS database instance.
- Configure a web application to use the new RDS database instance for data storage
- Test the application to ensure it is working with the new database.

## Screenshots

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/1.png)
Created a database instance under Amazon RDS

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/2.png)
Checking the status of MariaDB inside EC2 instance

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/3.png)
Webpage details

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/4.png)
Reviewing Databases and checking the tables inside of café_db

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/5.png)
Taking backup of the café_db database

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/6.png)
Modifying inbound rule to allow port 3306 and giving source as security group of EC2 instance


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/7.png)
Copying endpoint of RDS database


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/8.png)
3306 port is open


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/9.png)
Connecting to RDS database and reviewing the available databases


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/10.png)
Importing the Café_db backup to RDS Database



![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/11.png)
Secrets Manager details


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/12.png)
Stopping the MariaDB service inside the EC2 instance


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/13.png)
Accessing the webpage 


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/14.png)
Architecture diagram details before migration


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/15.png)
Architecture diagram details after migration 



## Conclusion
- Created an RDS database instance
- Exported data from a MariaDB database by using mysqldump
- Connected a SQL client to an RDS database.
- Migrated data from a MariaDB database that runs on an EC2 instance to an RDS database instance
- Configured a web application to use the new RDS database instance for data storage



