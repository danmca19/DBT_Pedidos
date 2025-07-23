Customer and Orders Data Modeling with dbt
This project presents a practical example of data modeling using dbt (Data Build Tool). It simulates a business scenario involving customers and orders, demonstrating how to apply transformations and business rules through SQL models and schema declarations. The goal is to showcase best practices for organizing, validating, and documenting analytical data pipelines.

➤ Project Overview
The objective is to build analytical models that transform raw customer and order data into reliable business insights. It includes filters, validation logic, and descriptive metadata to support real-world use cases such as dashboards, revenue analysis, and customer segmentation.

➤ Project Structure
clientes.sql
Transforms raw data from the tb_clientes table by selecting key fields like id_cliente, nome, email, status, and data_cadastro. This model defines the base customer dataset, supporting analytics related to customer behavior and onboarding.

pedidos.sql
Transforms data from tb_pedidos, including a filter that selects only orders where the valor_total is greater than 200. This models high-value transactions that are often key to marketing, sales, and strategic decisions.

schema.yml
YAML file that defines metadata and tests for each model. It includes descriptions of fields and validation rules such as unique and not null. This file enables automated testing and integrated documentation through dbt.

➤ Technical Approach
Models use Common Table Expressions (CTEs) for modular and readable SQL.

Business logic is applied directly in SQL (e.g., value filters).

Clear separation between raw and transformed layers.

Models are materialized as views for lightweight development and exploration.

Includes data tests to prevent issues such as duplicates or missing key values.

➤ Technologies Used
dbt (Data Build Tool) – for orchestrating SQL-based data transformations.

SQL – to encode business logic and data filters.

YAML – to declare schema definitions, field descriptions, and data quality tests.

➤ Real-World Applications
Customer and Order Analytics
This project can support dashboards and queries that explore:

Daily or weekly customer registrations

High-value order patterns

Customer lifecycle metrics and engagement

Revenue-Focused Business Insights
Filtering orders over a threshold helps prioritize marketing and sales efforts:

Identifying high-value customers

Monitoring revenue by time period or region

Supporting loyalty or retention campaigns based on order volume

➤ How to Run This Project
Clone the repository:

bash
Copiar
Editar
git clone <repository-url>
Set up your dbt environment and configure your profile connection.

Run the models:

bash
Copiar
Editar
dbt run
Run tests:

bash
Copiar
Editar
dbt test
Generate and serve the documentation:

bash
Copiar
Editar
dbt docs generate
dbt docs serve
➤ Next Steps
Create aggregate models such as customer lifetime value or average ticket size.

Introduce a staging layer to follow a layered approach: raw → staging → marts.

Add snapshots to capture historical changes in customer or order data.

Include advanced tests for value ranges, consistency, or business rule validation.

➤ References
dbt documentation: https://docs.getdbt.com

YAML specifications: https://yaml.org/spec/

Dimensional modeling (Kimball): The Data Warehouse Toolkit
