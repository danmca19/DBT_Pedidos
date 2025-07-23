# Customer and Orders Data Modeling with dbt

This project presents a practical example of data modeling using **dbt (Data Build Tool)**. It simulates a business scenario involving customers and orders, demonstrating how to apply transformations and business rules through SQL models and schema declarations. The goal is to showcase best practices for organizing, validating, and documenting analytical data pipelines.

## ➤ Project Overview

The objective is to build analytical models that transform raw customer and order data into reliable business insights. It includes filters, validation logic, and descriptive metadata to support real-world use cases such as dashboards, revenue analysis, and customer segmentation.

## ➤ Project Structure

- **clientes.sql**  
  Transforms raw data from the `tb_clientes` table by selecting key fields like `id_cliente`, `nome`, `email`, `status`, and `data_cadastro`. This model defines the base customer dataset, supporting analytics related to customer behavior and onboarding.

- **pedidos.sql**  
  Transforms data from `tb_pedidos`, including a filter that selects only orders where the `valor_total` is greater than 200. This models high-value transactions that are often key to marketing, sales, and strategic decisions.

- **schema.yml**  
  YAML file that defines metadata and tests for each model. It includes descriptions of fields and validation rules such as `unique` and `not null`. This file enables automated testing and integrated documentation through dbt.

## ➤ Technical Approach

- Models use **Common Table Expressions (CTEs)** for modular and readable SQL.
- Business logic is applied directly in SQL (e.g., value filters).
- Clear separation between raw and transformed data layers.
- Models are materialized as **views**, optimized for lightweight development and data exploration.
- Includes **automated tests** to ensure data quality and consistency.

## ➤ Technologies Used

- **dbt (Data Build Tool)** – for orchestrating and managing SQL transformations
- **SQL** – for implementing transformation logic and business rules
- **YAML** – for schema declarations, metadata, and automated testing

## ➤ Real-World Applications

### Customer and Order Analytics

This project supports dashboards and insights such as:
- New customer registrations over time
- High-value orders and purchasing behavior
- Customer lifecycle and engagement metrics

### Revenue-Oriented Business Use Cases

Filtering by order value enables focused analysis, including:
- Identifying and prioritizing top-spending customers
- Evaluating revenue trends across time and regions
- Supporting campaigns targeting high-ticket transactions



