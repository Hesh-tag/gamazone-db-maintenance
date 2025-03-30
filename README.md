
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

