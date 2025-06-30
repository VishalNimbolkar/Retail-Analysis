🛒 # Retail Analysis using PySpark
This project, Retail Analysis, is a PySpark-based data processing pipeline that performs analytical operations on retail datasets, including order and customer information. It demonstrates end-to-end capabilities of reading data, transforming it, aggregating insights, and validating outcomes through Pytest-based test suites.

##📂 Project Structure
bash
Copy
Edit
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

##🚀 Features
Reads customer and order data from CSVs

Filters only CLOSED orders

Joins orders with customer details

Aggregates number of closed orders by customer state

Environment-based configuration handling (LOCAL / TEST / PROD)

Unit tested using Pytest with tagging and skipping support

##⚙️ How to Run
1. Install Dependencies
bash
Copy
Edit
pipenv install
2. Activate the Environment
bash
Copy
Edit
pipenv shell
3. Run the Main Application
bash
Copy
Edit
python application_main.py LOCAL
4. Run Tests
bash
Copy
Edit
pytest --tb=short -v
You can also run specific tests using markers:

bash
Copy
Edit
pytest -m "latest"

##🧪 Sample Output
Upon successful execution, the program displays the count of closed orders grouped by customer state.

diff
Copy
Edit
+------------+-------------+
|customer_state|order_count|
+------------+-------------+
|      SP     |     1123   |
|      RJ     |      845   |
|     ...     |     ...    |
+------------+-------------+

##🛠️ Tech Stack
Language: Python 3

Big Data: Apache Spark (PySpark)

Testing: Pytest

Dependency Management: Pipenv

##📌 Key Learnings
Structuring PySpark projects modularly

Applying configuration-driven architecture

Writing efficient Spark transformations and actions

Practicing test-driven development with data pipelines

##📬 Contact
Feel free to connect or contribute via:

📧 Email: vishalnimbolkar10@gmail.com

🔗 LinkedIn Profile

🌟 Don't forget to ⭐ this repo if you find it useful!
