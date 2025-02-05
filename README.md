# Café Application Database Migration to Amazon RDS

This project demonstrates the migration of a café application's database from a local EC2 instance to Amazon RDS. The migration process includes exporting data from MariaDB on EC2, importing it into Amazon RDS, updating the application to use the new RDS endpoint, and verifying the application's functionality post-migration.

## Project Overview

### Key Tasks:
1. **Create an RDS Database Instance**:
   - Set up an Amazon RDS instance to host the café application database.

2. **Export Data from EC2 MariaDB**:
   - Use `mysqldump` to export the database from the EC2 instance.

3. **Migrate Data to RDS**:
   - Import the exported data into the RDS database.

4. **Update Application Configuration**:
   - Modify the application to use the RDS endpoint for database connectivity.

5. **Test the Application**:
   - Verify that the application functions correctly with the new RDS database.

## Technologies Used
- **AWS EC2**: Hosted the original MariaDB database.
- **Amazon RDS**: Hosted the migrated database.
- **PHP**: Used for the café application.
- **MariaDB**: Database management system.
- **AWS Secrets Manager**: Securely managed database credentials.

## Steps

### 1. Create an RDS Database Instance
- Set up an Amazon RDS instance with MariaDB.

### 2. Export Data from EC2 MariaDB
- Use the `mysqldump` command to create a backup of the `café_db` database.

### 3. Migrate Data to RDS
- Connect to the RDS instance using an SQL client.
- Import the backup file into the RDS database.

### 4. Update Application Configuration
- Modify the application's database connection settings to use the RDS endpoint.
- Store database credentials securely using AWS Secrets Manager.

### 5. Test the Application
- Stop the MariaDB service on the EC2 instance.
- Verify that the application functions correctly with the RDS database.

---

## Screenshots

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/1.png)

Created RDS Database Instance

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/2.png)

Checking MariaDB Status on EC2

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/3.png)

Café Application Webpage

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/4.png)

Reviewing Databases and Tables

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/5.png)

Taking backup of the café_db database

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/6.png)

Modifying inbound rule to allow port 3306 and giving source as security group of EC2 instance

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/7.png)

Copying endpoint of RDS database

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/8.png)

Verifying Open Port 3306

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/9.png)

Connecting to RDS and Reviewing Databases

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/10.png)

Importing the Café_db backup to RDS Database

$~$


![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/11.png)

AWS Secrets Manager Configuration

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/12.png)

Stopping MariaDB on EC2 Instance

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/13.png)

Accessing the Webpage Post-Migration

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/14.png)

Architecture Diagram (Before Migration)

$~$

![Alt text of the image](https://github.com/BasilTAlias/AWS-DB-Migration/blob/main/images/15.png)

Architecture Diagram (After Migration)

$~$

## Conclusion

- Successfully created an **Amazon RDS** database instance.
- Exported data from a **MariaDB** database using `mysqldump`.
- Connected an **SQL client** to the RDS database.
- Migrated data from an EC2-hosted **MariaDB** database to RDS.
- Configured the web application to use **Amazon RDS** as its database backend.



