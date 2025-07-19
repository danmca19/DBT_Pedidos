# Customer and Orders Data Modeling with dbt

This project demonstrates a simple yet practical example of data modeling using **dbt (Data Build Tool)**. It was designed to simulate a business case involving customers and orders, showcasing data transformation and filtering logic through SQL models and schema definitions.

---

## 🧩 Project Structure

- `clientes.sql`: Models the customer data from the raw table `tb_clientes`, selecting relevant fields such as ID, name, email, status, and registration date.
- `pedidos.sql`: Models the orders data from the raw table `tb_pedidos`, filtering only orders where the total value is greater than 200.
- `schema.yml`: Contains metadata definitions for both models, including descriptions and testing configurations (e.g., for unique and not null fields).

---

## 🔍 Key Features

- Uses **CTEs (Common Table Expressions)** to modularize transformations.
- Applies a **filtering rule** for order value (`valor_total > 200`) to illustrate business logic.
- Materialized as **views**, optimizing for data exploration rather than storage.
- Provides clear separation between raw and modeled data.

---

## 🛠️ Technologies Used

- **dbt (Data Build Tool)** – for data transformation and modeling
- **SQL** – to create business logic and data filters
- **YAML** – for schema definitions and data validation

---

## 📊 Real-World Applications

### Example 1 – Customer Segmentation Dashboard
These models could be used to build a dashboard that monitors:
- New customer registrations
- High-value orders (above $200)
- Customer activity and engagement over time

### Example 2 – Revenue Insights for Marketing
By filtering orders over a threshold, this model helps marketing teams focus on:
- High-revenue clients
- Time periods with the highest sales
- Regional trends in spending behavior

---

## 🚀 Getting Started

1. Clone this repository
2. Set up your dbt project environment
3. Run the models using:
   ```bash
   dbt run
