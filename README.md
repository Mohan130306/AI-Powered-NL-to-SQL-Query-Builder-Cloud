#  AI-Powered Natural Language to SQL Query Builder

##  Project Overview

The AI-Powered Natural Language to SQL Query Builder is an intelligent database assistant that enables users to interact with a SQLite database using plain English instead of writing SQL queries manually.

The application leverages the Mistral Large Language Model (LLM) through Ollama to convert natural language questions into SQL queries, validate them using a safety layer, execute them on a SQLite database, and present the results in a user-friendly interface.

This project demonstrates the integration of Artificial Intelligence, Database Management, and Web Application Development to simplify data access for non-technical users.

---

#  Problem Statement

Most users do not know SQL and cannot directly query databases.

Retrieving information from databases typically requires technical expertise, forcing non-technical users to depend on database administrators or developers.

This project eliminates that barrier by allowing users to ask questions in plain English while the AI automatically generates and executes the corresponding SQL query.

Example:

### User Input

Show all students with CGPA above 8.5

### AI Generated SQL

SELECT * FROM students WHERE cgpa > 8.5;

### Output

Displays all matching student records.

---

#  Features

### AI-Powered SQL Generation

* Converts natural language into SQLite queries.
* Uses Ollama + Mistral LLM.

### Dynamic Schema Reading

* Reads database schema automatically.
* Provides schema context to the AI model.

### Query Safety Validation

* Allows only SELECT queries.
* Blocks dangerous operations.

### Database Query Execution

* Executes safe SQL queries on SQLite.

### Interactive Dashboard

* Built using Streamlit.
* User-friendly interface.

### Query History

* Stores previously executed queries.

### CSV Export

* Download query results as CSV files.

### AI Workflow Demonstration

* End-to-end AI-powered database interaction.

---

#  System Architecture

User Question

↓

Schema Reader

↓

Mistral AI Model

↓

SQL Generator

↓

Safety Checker

↓

SQLite Database

↓

Results Display

↓

Explanation

---

#  Technology Stack

| Component            | Technology  |
| -------------------- | ----------- |
| Programming Language | Python 3.11 |
| Frontend             | Streamlit   |
| Database             | SQLite      |
| AI Model             | Mistral     |
| AI Runtime           | Ollama      |
| Data Processing      | Pandas      |
| IDE                  | VS Code     |

---

#  Project Structure

sql-query-builder/

├── app.py

├── README.md

├── requirements.txt

│

├── database/

│ ├── create_db.py

│ └── college.db

│

├── ai/

│ ├── schema_reader.py

│ ├── sql_generator.py

│ ├── safety_checker.py

│ └── query_executor.py

│

├── tests/

│ └── test_pipeline.py

│

├── docs/

│ └── ai_usage_note.md

│

└── sample_data/

---

#  Installation

## Clone Repository

git clone <repository-url>

cd sql-query-builder

## Create Virtual Environment

python -m venv venv

## Activate Environment

Windows:

venv\Scripts\activate

## Install Dependencies

pip install -r requirements.txt

---

#  Running the Application

## Create Database

python database/create_db.py

## Launch Streamlit

streamlit run app.py

---

#  Sample Queries

Try the following questions:

### Query 1

Show all CSE students

### Query 2

Show students with CGPA above 8.5

### Query 3

Show top 5 students by CGPA

### Query 4

Count students in ECE

### Query 5

Show final year students

---

#  Safety Features

Allowed:

* SELECT

Blocked:

* INSERT
* UPDATE
* DELETE
* DROP
* ALTER
* TRUNCATE
* ATTACH
* PRAGMA

Example:

User Input:

Delete all students

Result:

❌ Unsafe Query Blocked

---

#  Testing

The project includes test scripts to verify:

* SQL Generation
* Query Safety
* Query Execution
* End-to-End Workflow

Run:

python tests/test_pipeline.py

---

#  Future Enhancements

* Support for multiple databases
* Role-based access control
* Query visualization dashboards
* Voice-based database querying
* Advanced AI explanations
* Cloud deployment

---

#  Learning Outcomes

* Prompt Engineering
* AI Agent Workflows
* SQLite Database Integration
* Streamlit Application Development
* Query Safety Validation
* LLM Integration using Ollama

---

#  Team Members

Team Size: 3 Members

Team Members: Mohan Kumar A, Moneesh Shivakumar S, Ragul Gandhi B

Project: AI-Powered Natural Language to SQL Query Builder

---

#  License

This project was developed for Infinite Computer Solutions Round 3 .
