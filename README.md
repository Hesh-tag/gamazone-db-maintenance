
# Gamazone Database Management with Amazon RDS and PostgreSQL
This project manages the PostgreSQL database for the Gamazone e-commerce platform, hosted on **Amazon RDS**. It includes the initial schema setup, sample data insertion, backup/restore procedures, and connection details.

---

## 🎯 Project Overview
- **Database Engine:** PostgreSQL (hosted on Amazon RDS)
- **Schema:** Tables for users, products, categories, orders, payments, and inventory.
- **Focus Areas:**
  - Secure database management
  - Basic schema setup
  - Sample data insertion
  - Access Control
  - Backup and restore procedures

---

## 🚀 Getting Started

### Clone the Repository
```bash
git clone https://github.com/your-username/gamazone-rds-postgresql-db-management.git
cd gamazone-rds-postgresql-db-management
```

---

### Connect to PostgreSQL on Amazon RDS
```bash
# Run the connection script
./connect-to-db.sh
```
Or, to connect manually:
```bash
psql -h gamazone-db-instance.c9m8q0yekuoq.us-east-2.rds.amazonaws.com -U gamazone_admin -d gamazone_db
```

---

### Create PostgreSQL Database
```sql
CREATE DATABASE gamazone_db;
```

---

![Database ERD](./resources/entity_relationship.png)

### Run Database Schema
```sql
\i D:/awsprojects/gamazone-db-maintenance/gamazone_schema.sql
```

---

### Verify Tables
```sql
\dt
```

## 📂 Database Structure
### 1. Users Table
- Stores user information such as name, email, and password.

### 2. Products Table
- Stores product details, including name, category, and price.

### 3. Orders Table
- Maintains order information with total amount and order status.

### 4. Order Items Table
- Contains items associated with each order.

### 5. Payments Table
- Stores payment details and transaction history.

### 6. Inventory Table
- Manages stock quantity and product availability.

---

## 📄 Sample Data
The `sample_data.sql` file contains realistic sample data for testing and showcasing functionality.

---

## 🚀 How to Run the SQL Script
To insert sample data into the database:
```bash
psql -U your_username -d gamazone_db -f D:/awsprojects/gamazone-db-maintenance/sample_data.sql

# 📚 Setting Up pgAdmin to Connect to Amazon RDS PostgreSQL

---

## ⚡️ Step 1: Download and Install pgAdmin
1. Go to the [pgAdmin Download Page](https://www.pgadmin.org/download/).
2. Download and install the appropriate version for your operating system (Windows, macOS, or Linux).
3. Follow the installation instructions to complete the setup.

---

## ⚡️ Step 2: Launch pgAdmin
1. Open pgAdmin after installation.
2. The pgAdmin interface will load in your default browser.

---

## ⚡️ Step 3: Create a New Server in pgAdmin
1. In the pgAdmin dashboard, right-click on **Servers** in the left panel.
2. Select **Create** → **Server**.
3. In the **General** tab:
   - **Name:** Enter a name for your server (e.g., `Gamazone Database`).

---

## ⚡️ Step 4: Configure Connection Settings
1. Click on the **Connection** tab.
2. Enter the following details:
   - **Host name/address:** Your Amazon RDS endpoint (e.g., `your-db-instance.xxx.us-east-1.rds.amazonaws.com`).
   - **Port:** `5432` (default PostgreSQL port).
   - **Maintenance database:** `postgres` or the name of your database (e.g., `gamazone_db`).
   - **Username:** Your master username created during RDS setup.
   - **Password:** The password for the RDS master user.
3. Click **Save** to create the connection.

---

## ⚡️ Step 5: Test the Connection
1. After saving the server configuration, expand the newly created server.
2. Click on **Databases** and select your database to view and manage tables, run queries, and perform database operations.

---
![Pgadmin ERD](./resources/pgadmin .png)

---