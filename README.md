# 🤖 Text to SQL 

Welcome to the **Text to SQL Chatbot** project! This project aims to bridge the gap between non-technical team members and database interactions, allowing users to query databases using **natural language instead of SQL**.

## 📚 Table of Contents

- [📖 Project Overview](#-project-overview)
- [🔧 Features](#-features)
- [🛠️ Installation](#️-installation)
- [🚀 Usage](#-usage)
- [🗼 Architecture](#-architecture)
- [📊 Evaluation](#-evaluation)
- [📝 Future Work](#-future-work)
- [📄 License](#-license)

## 📖 Project Overview

In many companies, team members may need access to data stored in SQL databases but lack the technical skills to write SQL queries. This chatbot allows users to ask questions in **natural language**, converts those questions into **SQL queries**, and retrieves results from the database.

This project can be applied across various domains, including:

- Healthcare
- Retail
- Finance
- Business Analytics
- Customer Data Analysis

## 🔧 Features

- **Natural Language Processing**: Converts user queries into SQL statements.
- **Database Interaction**: Connects to MySQL databases to fetch relevant results.
- **User-Friendly Output**: Presents database results in an easy-to-understand format.
- **End-to-End Solution**: Covers the complete workflow from data preparation to natural-language interaction.
- **LLM-Powered Query Generation**: Uses a Large Language Model to understand user questions and generate SQL queries.
- **Dynamic Database Querying**: Executes generated SQL queries directly against the connected database.

## 🛠️ Installation

Follow these steps to set up the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Text-to-SQL-Chatbot.git
cd Text-to-SQL-Chatbot
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the virtual environment:

**Windows:**

```bash
venv\Scripts\activate
```

**macOS/Linux:**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up MySQL

- Install and configure MySQL.
- Create a MySQL database.
- Create the required tables.
- Load your dataset into the database.
- Update the database connection details in the project configuration.

### 5. Configure API Keys

Add the required API keys for the LLM used by the application.

Create a `.env` file in the project root:

```env
GOOGLE_API_KEY=your_api_key_here
```

> **Note:** Never commit your API keys or `.env` file to GitHub.

## 🚀 Usage

After completing the installation and configuration steps, run the application using:

```bash
python app.py
```

The Flask application will start locally. Open the URL shown in the terminal in your web browser.

You can then enter questions such as:

```text
What are the total sales for each product?
```

The chatbot converts the natural-language question into an SQL query, executes it against the MySQL database, and returns the result in a user-friendly format.

## 🗼 Architecture

The architecture of the Text to SQL Chatbot consists of the following major components:

```text
User
  │
  ▼
Natural Language Question
  │
  ▼
Large Language Model
  │
  ▼
SQL Query Generation
  │
  ▼
MySQL Database
  │
  ▼
Query Execution
  │
  ▼
Retrieved Results
  │
  ▼
Natural Language Response
  │
  ▼
User
```

### Components

- **Data Source**: Excel sheets containing raw data.
- **Database**: MySQL database where the structured data is stored.
- **LLM Chain**: Uses a Large Language Model to convert natural-language questions into SQL queries.
- **SQL Query Execution**: Executes the generated SQL query against the MySQL database.
- **Output Parser**: Processes the query results and formats them for user-friendly presentation.
- **Web Interface**: Provides an interactive interface for users to communicate with the chatbot.

### Architecture Diagram

Add your architecture diagram to the repository and update the path below:

```markdown
![Text to SQL Chatbot Architecture](assets/architecture.png)
```

## 📊 Evaluation

The performance of the chatbot can be evaluated using several metrics:

- **SQL Accuracy**: Measures how accurately the LLM generates the required SQL queries.
- **Response Time**: Measures the time required to generate and execute a query and return the result.
- **User Feedback**: Evaluates the clarity, relevance, and usefulness of the chatbot's responses.
- **Query Reliability**: Measures the chatbot's ability to correctly handle different types of natural-language queries.

## 📝 Future Work

Several improvements can be made to enhance the project:

- **Advanced Query Validation**: Add additional validation and error-handling mechanisms for generated SQL queries.
- **Improved User Interface**: Enhance the web interface using Flask, Streamlit, or other modern UI frameworks.
- **Conversation Memory**: Enable the chatbot to understand follow-up questions using conversational context.
- **Cloud Deployment**: Deploy the application on cloud platforms for public accessibility.
- **Database Expansion**: Support multiple databases and larger datasets.
- **Performance Optimization**: Improve query generation and execution speed.
