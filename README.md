# UniSQLBot 🤖

> Bridge between Natural Language and SQL Queries

UniSQLBot is a Streamlit-based web application that converts natural language questions into SQL queries for SQLite databases. It allows users to interact with their databases using plain English instead of writing SQL code.

## 🌟 Features

- **Natural Language to SQL Conversion**: Ask questions in plain English and get SQL queries automatically generated
- **Query Execution**: Automatically executes the generated SQL queries against your selected database
- **Results Visualization**: Visualizes query results with appropriate charts when applicable
- **Conversation History**: Maintains a history of your queries and results
- **Database Upload**: Upload your own SQLite databases or use the provided sample database
- **Dark Theme UI**: Modern dark-themed user interface for comfortable usage

## 📋 Requirements

- Python 3.7+
- OpenAI API key
- Streamlit
- Pandas
- Matplotlib
- Seaborn
- SQLite3
- OpenAI Python client

## 🚀 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/UniSQLBot.git
   cd UniSQLBot
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a directory for databases:
   ```bash
   mkdir -p ./databases
   ```

## 🏃‍♂️ Running the Application

Run the application with:

```bash
streamlit run main_app.py
```

The application will be available at `http://localhost:8501` in your web browser.

## 💼 Usage

1. **Enter your OpenAI API key** in the sidebar
2. **Select a database** from the dropdown or upload your own SQLite database
3. **Ask a question** in plain English about your data
4. **Click "Generate SQL & Execute"** to process your query
5. View the **generated SQL query and results** in the main panel

### Example Questions

For the sample academic database:
- "Show all authors and their publications"
- "How many publications does each author have?"
- "Which authors published papers in 2022?"
- "List the publications with their authors sorted by year"

## 📊 Database Schema

The application automatically extracts and displays the schema of the selected database in the sidebar, showing tables and their columns.

## 🧩 Architecture

- **main_app.py**: Main application file containing the Streamlit UI and core functionality
- **./databases/**: Directory for storing SQLite database files

## 🛠️ Core Functions

- `get_db_schema()`: Extracts schema information from a SQLite database
- `process_natural_language_query()`: Converts natural language to SQL using OpenAI API
- `execute_sql_query()`: Executes SQL queries against the database
- `extract_sql_query()`: Extracts SQL from the OpenAI API response

## 📝 Notes

- The application uses OpenAI's GPT-3.5 Turbo model for natural language processing
- A valid OpenAI API key is required for the application to function
- The application supports SQLite databases with extensions `.sqlite`, `.db`, `.sqlite3`, and `.db3`

## 🔒 Security

- API keys are stored only in the session and not persisted
- The application runs locally, and your data doesn't leave your machine except for the natural language queries sent to OpenAI

## 👥 Credits

UniSQLBot was developed by:

- Ajay Rallapalli
- Sai Mahitha Etikala
- Sai Rathnakar Reddy Paderla

This project was developed as part of the DS5983 SPTP: Large Language Models course at Northeastern University.

## 📄 License

[MIT License](LICENSE)
