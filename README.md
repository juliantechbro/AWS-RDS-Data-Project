# AWS-Database
 
## Overview

This project walks through the process of setting up a secure AWS RDS instance using IAM roles and security groups, importing a dataset from Kaggle into MySQL, and creating visualizations using Amazon QuickSight. The goal is to demonstrate end-to-end cloud database management, security best practices, and data visualization skills.

![AWS Banner](https://github.com/user-attachments/assets/88f62300-9370-4ef0-a94e-274864c74a20)


## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Media](#media)
- [Contributing](#contributing)
- [License](#license)


## Features
- **Secure AWS RDS Setup:** Use IAM roles and security groups to ensure secure access.
- **Kaggle Dataset Integration:** Import and analyze a real-world dataset from Kaggle.
- **Data Visualization:** Create interactive dashboards using Amazon QuickSight.
- **Scalability:** Demonstrates how AWS RDS can handle larger datasets.


## Technologies Used
- **Cloud Provider:** Amazon Web Services (AWS)
- **Database:** Amazon RDS (MySQL)
- **Data Visualization:** Amazon QuickSight
- **Dataset Source:** Kaggle
- **Security:** AWS IAM Roles, AWS Security Groups
- **Other Tools:** AWS Management Console, MySQL Workbench, Kaggle API
<hr>

## Step-by-Step Guide
1. Set Up IAM Roles and Security Groups
<br><br>IAM (Identity Access Management) controls access throughout the AWS console. AWS recommends working through an 
IAM role instead of the root account. I setup various user groups, roles, and attached the policies that would connect with 
the tools we're using.

![User Groups](https://github.com/user-attachments/assets/30865f7e-e440-4e03-90bf-8932ef2066a1)

After creating the various IAM roles, I went to create the security groups which would control access to our database and data resources.
Here we create a security group specifically for the RDS service so that we can control access to the database. It was important for me to 
ensure the database was publicly accessible and then adjust the security group so that only my IP address could be let into the database.


![Create Security Group](https://github.com/user-attachments/assets/a38d8b01-e89a-4ae8-bddc-0756497ffc8f)

<hr>

2. Create an AWS RDS Instance
<br><br> Next I created a database instance through AWS RDS which has been renamed to Aurora and RDS in the console. It was important to select the MySQL,
the instance size, and the password for the database which we'll use to connect with MySQL. The database took a few minutes to create, it's not available until
it says that the database is available. 


![Create Database](https://github.com/user-attachments/assets/f4773ec3-85ce-4038-a9ac-27622e63a67b)

<hr>
 
3. Connect MySQL to the RDS Instance
<br><br>Next I proceeded to connect the AWS database instance with MySQL. I received a few errors but this was due to the fact that I needed to wait for the database to
complete updating. I learned as long as the database is publicly accessible and I set the correct security group settings, it will go through.

![Connect from AWS TO MySQL](https://github.com/user-attachments/assets/7e7fc024-84bc-4bfa-8c73-6048246b3514)

<hr>

4. Import Dataset into MySQL
<br><br> Afterwards, I imported the dataset into the database through MySQL's data import wizard. It was very intuitive. I would say in the future, I would make sure to
create proper database structure beforehand. In excel, you can create the different sheets to correspond with each table in the database and ensure that the column headers is
properly formatted.

![Import CSV into MySQL](https://github.com/user-attachments/assets/4675719a-cc7f-484e-8544-6e432fad0c70)
<hr>

