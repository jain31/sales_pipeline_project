# Automated Sales ETL Pipeline & Analytics Dashboard

An end-to-end data engineering and analytics project designed to ingest, clean, quarantine, and visualize sales transactions seamlessly. This project simulates an enterprise ETL architecture using Python, Pandas, SQLite, Streamlit, and Apache Airflow.

##  Key Features
Sales Frontend Portal: An interactive Streamlit web form for salespersons to log transaction records easily.
Raw Landing Zone: Automatically appends form submissions to an uncleaned raw CSV file (`ingestion/raw_sales.csv`).
Automated Data Cleaning & Validation: A modular pipeline script (`pipeline.py`) that standardizes text fields, handles missing values, and calculates metrics.
Error Isolation (Quarantine):Automatically catches malformed or incomplete records and routes them to a dedicated quarantine file (`quarantine/bad_records.csv`) to prevent data corruption.
Structured Storage: Persists clean, validated data into a relational SQLite database (`db/sales.db`).
Workflow Orchestration:Automated scheduling and execution support via Apache Airflow DAGs (`dag.py`).
Analytics Dashboard: A multi-tab Streamlit interface rendering real-time business metrics, regional revenue breakdowns, and daily sales trends.

---

##  Project Directory Structure


sales_pipeline_project/
│
├── db/
│   └── sales.db       
├── ingestion/
│   └── raw_sale  
├── logger_file/
│   └── pipeline.log             
├── null_values/       
├── parsers/
│   └── clean_parser.py            
├── quarantine/
│   └── bad_records.csv            
├── src/
│   └── app.py                    
├── dag.py                         
├── pipeline.py                    
├── requirements.txt               
└── setup_infrastructure.py       