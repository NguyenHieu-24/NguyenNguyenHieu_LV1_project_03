# Data Migration & ETL Project
## 📌 Project Overview

This project is a Level 1 Data Engineering ETL & Database Migration system designed to migrate and load structured business data into a relational database (SQL Server).

The system follows a modular ETL approach, including:
- Database schema migration using SQL scripts
- Data loading using Python
- Connection testing and validation
- Clear separation between migration logic and data loaders

This project demonstrates fundamental Data Engineer skills, including database design, ETL pipelines, Python scripting, and SQL-based migrations.

## 🏗️ Project Structure
NguyenNguyenHieu_LV1_project_03/
│
├── main.py                     # Main entry point to run ETL pipeline
├── migrate.py                  # Executes database migration scripts
├── test_connection.py          # Tests SQL Server connection
├── requirements.txt            # Python dependencies
│
├── migrations/                 # SQL migration scripts (DDL)
│   ├── 01_migrate_brand.sql
│   ├── 02_migrate_category.sql
│   ├── 03_migrate_seller.sql
│   ├── 04_migrate_product.sql
│   ├── 05_migrate_order.sql
│   ├── 06_migrate_order_item.sql
│   ├── 07_migrate_promotions.sql
│   └── 08_migrate_promotion_products.sql
│
├── loaders/                    # Python ETL loaders (DML)
│   ├── load_brand.py
│   ├── load_category.py
│   ├── load_seller.py
│   ├── load_product.py
│   ├── load_order.py
│   ├── load_order_item.py
│   ├── load_promotion.py
│   └── load_promotion_product.py
│
└── README.md

## ⚙️ Technologies Used

- Python 3.10+
- Microsoft SQL Server
- pyodbc
- Poetry / pip
- SQL (DDL & DML)

## 🧠 Data Model

The database schema includes the following core business entities:
- Brand
- Category
- Seller
- Product
- Order
- Order Item
- Promotion
- Promotion Product
- Relationships are designed using foreign keys to ensure data integrity and normalization.

## 🚀 How to Run the Project
### 1️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
Or using Peotry:
```bash
poetry install
```

### 2️⃣ Configure Database Connection
Update the database connection settings inside:
```bash
test_connection.py
```
Ensure:
- SQL Server is running
- Database exists
- Credentials are correct

### 3️⃣ Test Database Connection
```bash
python test_connection.py
```

### 4️⃣ Run Database Migrations
```bash
python migrate.py
```
This will:
- Create tables
- Apply schema changes in correct order

### 5️⃣ Run ETL Pipeline
```bash
python main.py
```

This will:
- Load data into each table
- Maintain referential integrity
- Complete the ETL process

## ✅ Key Features
- Modular ETL design
- SQL-based schema migration
- Clean separation of concerns
- Easy to extend with new entities
- Production-style folder structure

## 📈 Skills Demonstrated
- Data Modeling & Normalization
- SQL Server schema migration
- Python-based ETL pipelines
- Database connectivity & testing
- ETL best practices

## 📄 License
This project is for educational and learning purposes.
