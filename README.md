# Delta Lake MERGE Implementation

Hey there! This repo holds my work for Assignment 7 during my internship at Celebal Technologies. 

For this task, I focused on handling incremental data updates using Delta Lake and Spark. Instead of overwriting entire tables every time new data comes in, I used the powerful `MERGE INTO` command to efficiently upsert (update existing records and insert new ones) data.

## What I Did

* **Data Prep & Cleaning:** Loaded up our initial customer master dataset into a Delta table, handled any messy null values, and cleaned out duplicates.
* **Simulating Incremental Data:** Brought in a second incremental dataset containing brand new customer info and updates to existing entries.
* **Executing the Merge:** Wrote out the Delta Lake merge logic to match IDs, update older records, and append the fresh ones.
* **Validation & Checks:** Double-checked row counts and verified that everything merged cleanly without duplicating data.

## Repository Layout

```text
delta-lake-assignment/
│
├── data/
│   ├── customer_master.csv
│   └── customer_incremental.csv
│
├── notebooks/
│   └── delta_scd_assignment.ipynb
│
├── screenshots/
│   ├── data_loading/
│   ├── data_cleaning/
│   ├── scd1/
│   ├── scd2/
│   ├── validation/
│   └── final_output/
│
├── report/
│   └── assignment_summary.pdf
│
└── README.md
