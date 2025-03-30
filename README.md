
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

### Run Database Schema
```sql
\i D:/awsprojects/gamazone-db-maintenance/gamazone_schema.sql
```

---

### Verify Tables
```sql
\dt
```

---

# Gamazone Database Maintenance Project

This project contains a PostgreSQL database setup for **Gamazone**, an e-commerce platform specializing in gaming equipment. The database includes tables for users, products, orders, order items, payments, and inventory.

## 📚 Project Overview
- **Database Name:** `gamazone_db`
- **Technology:** PostgreSQL hosted on Amazon RDS
- **Focus Areas:**
  - Access Control
  - Security Measures
  - Data Backup and Maintenance

---

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

