# ⚡ Kafka Heavy Workflow with Python + Docker + Schema Registry

📌 This project demonstrates a heavy workflow using Apache Kafka with multiple consumers, producers, and schema registry integration for real-time and batch log processing.

---

## 🚀 Project Overview
This project simulates a **retail database pipeline** using Apache Kafka.  
It streams data from different retail domains (orders, customers, products, departments, categories, order_items), consumes messages with Python consumers, validates schemas using Confluent Schema Registry, and stores logs in dedicated directories for further analysis.

The workflow is designed to show how large-scale event-driven pipelines can be managed and scaled.

---

## 🧰 Tech Stack
- **Language**: Python  
- **Streaming Platform**: Apache Kafka (via Docker Compose)  
- **Schema Management**: Confluent Schema Registry  
- **Storage**: File-based logs (batch + streaming simulation)  
- **Libraries**:  
  - `confluent-kafka` – Kafka producer/consumer client  
  - `fastavro` / `avro-python3` – Avro schema handling (if used)  
  - `pandas` – Optional transformations  
  - `requests` – For API calls if needed  
  - `python-dotenv` – Load environment configs  

---

## 📦 Project Structure
```text
kafka_heavy_workflow/
├── categories_logs_batch/         # Batch logs for categories
├── customers/                     # Customers-related logs
├── departments_logs/              # Departments logs
├── docker-compose.yml             # Spins up Kafka, Zookeeper, Schema Registry
├── main.py                        # Main entry point for workflow orchestration
├── models.py                      # Python models (data structures/schemas)
├── order_items_logs/              # Order items logs
├── orders_logs/                   # Orders logs
├── products_logs/                 # Products logs
├── pyconsumer_categories.py       # Kafka consumer for categories
├── pyconsumer_customers.py        # Kafka consumer for customers
├── pyconsumer_departments.py      # Kafka consumer for departments
├── pyconsumer_oi.py               # Kafka consumer for order_items
├── pyconsumer_orders.py           # Kafka consumer for orders
├── pyconsumer_products.py         # Kafka consumer for products
├── readme.txt                     # Initial notes
├── requirements.txt               # Python dependencies
├── retail_db/                     # Sample retail database (reference)
├── schema_registry.py             # Schema Registry integration
├── schemas.py                     # Avro/JSON schemas for topics
└── test/                          # Test scripts
project_tree.txt                   # Full project tree (auto-generated)
tree_top2.txt                      # High-level tree (top 2 levels)
