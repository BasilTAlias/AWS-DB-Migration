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
•	Create an RDS database instance.
•	Export data from a MariaDB database by using mysqldump.
•	Connect an SQL client to an RDS database.
•	Migrate data from a MariaDB database that runs on an EC2 instance to an RDS database instance.
•	Configure a web application to use the new RDS database instance for data storage
• Test the application to ensure it is working with the new database.


