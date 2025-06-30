# Retail Analysis using PySpark
This project, Retail Analysis, is a PySpark-based data processing pipeline that performs analytical operations on retail datasets, including order and customer information. It demonstrates end-to-end capabilities of reading data, transforming it, aggregating insights, and validating outcomes through Pytest-based test suites.

## Project Structure
```
Retail_Analysis/
├── application_main.py           # Main execution script
├── conftest.py                   # Pytest fixture configuration
├── test_retail_project.py       # Unit tests for core functionalities
├── configs/
│   └── application.conf         # Environment-wise config paths
├── lib/
│   ├── DataReader.py            # Data ingestion utilities
│   ├── DataManipulation.py      # Data transformation and aggregation logic
│   ├── Utils.py                 # Spark session and general utilities
│   └── ConfigReader.py         # Application config reader
├── data/
│   ├── customers.csv            # Sample customer data
│   └── orders.csv               # Sample orders data
├── Pipfile & Pipfile.lock       # Environment and dependency management
└── pytest.ini                   # Pytest configuration

```

## Features

1. Reads customer and order data from CSVs
2. Filters only CLOSED orders
3. Joins orders with customer details
4. Aggregates number of closed orders by customer state
5. Environment-based configuration handling (LOCAL / TEST / PROD)
6. Unit tested using Pytest with tagging and skipping support

## How to Run

### 1. Install Dependencies

```
pipenv install
```
### 2. Activate the Environment

```
pipenv shell
```

### 3. Run the Main Application

```
python application_main.py LOCAL
```

### 4. Run Tests

```
pytest -m "latest"
```


## Sample Output

Upon successful execution, the program displays the count of closed orders grouped by customer state.

```
+------------+-------------+
|customer_state|order_count|
+------------+-------------+
|      SP     |     1123   |
|      RJ     |      845   |
|     ...     |     ...    |
+------------+-------------+
```

## Tech Stack

1. Language: Python 3
2. Big Data: Apache Spark (PySpark)
3. Testing: Pytest
4. Dependency Management: Pipenv

## Key Learnings

1. Structuring PySpark projects modularly
2. Applying configuration-driven architecture
3. Writing efficient Spark transformations and actions
4. Practicing test-driven development with data pipelines

###  Don't forget to ⭐ this repo if you find it useful!


