# Finance_financetracker_30211
Simple expense and revenue tracker
Financial Tracker: A Simple Revenue & Expense App
This is a user-friendly financial tool built with Python, Streamlit, and a PostgreSQL database. It's designed to give you a clear, simple way to track your finances, whether for personal use or for a small business.

Key Features ✨
Data Management: Easily add new transactions, view all records, and delete unwanted entries. You can also filter the list by type (Revenue/Expense) and sort it by amount or date.

Financial Insights: The app provides a dashboard with real-time metrics, including the total number of transactions, total revenue, and total expenses. Most importantly, it calculates your Net Income for a quick financial summary.

Getting Started 🚀
To run this application, you'll need a few things set up first.

1. Prerequisites

Python 3.x

A running PostgreSQL database instance.

The required Python libraries. You can install them with this command:

Bash

pip install streamlit psycopg2-binary pandas
2. Database Setup

Create a new database in your PostgreSQL server.

Execute the following SQL command to create the transactions table. This is a one-time step.

SQL

CREATE TABLE transactions (
    transaction_id VARCHAR(255) PRIMARY KEY,
    transaction_date DATE NOT NULL,
    description TEXT,
    amount DECIMAL(10, 2) NOT NULL,
    type VARCHAR(20) CHECK (type IN ('Revenue', 'Expense'))
);
File Structure 📂
The application is cleanly organized into two files:

Frontend_fin.py: This file handles the user interface and app layout using Streamlit.

Backend_fin.py: This file contains all the core logic, including database connections and functions for data management and analysis.

How to Run 💻
Open Backend_fin.py and update the database credentials (username, password, etc.) to match your PostgreSQL setup.

Save both Frontend_fin.py and Backend_fin.py in the same directory.

Open your terminal, navigate to that directory, and run the following command:

Bash

streamlit run Frontend_fin.py
The application will automatically open in your web browser.

Possible Enhancements 💡
This app is a great starting point, and you could add more features such as:

A feature to edit existing transactions.

Data visualization with charts (e.g., monthly revenue vs. expenses).

User authentication for secure, multi-user access.

Transaction categories to better organize your finances.
