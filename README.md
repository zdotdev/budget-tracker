# Budget Tracker Documentation

## Overview

The Budget Tracker is a web-based application designed to help users track their income and expenses. The application allows users to add budget items, view total balance, and check records of their financial transactions. The application is built using HTML, CSS, and JavaScript for the frontend, and Node.js, Express, and MySQL for the backend.

## User Interface

The user interface is divided into two main sections:

1.	Budget item form: This section allows users to add a new budget item by specifying its type (income or expense), category, note, amount, and date.
2.	Records and total balance: This section shows the total balance and a list of all budget items that have been added.

The HTML code for the user interface is in the index.html file.

## JavaScript Functions

The JavaScript code is in the index.js file and contains several functions to handle different parts of the application:
- `setCurrentDate()` Sets the current date in the date input field.
- `handleTypeSelect()` Handles the change event of the type select element to populate the category options.
- `fetchAndCalculateBalance()` Fetches all budget items from the backend and calculates the total balance.
- `fetchAndDisplayRecords()` Fetches and displays all the records.
- `handleFormSubmission()` Handles the form submission event to add a new budget item.

## Backend Server

The backend server is built using Node.js and Express. It provides several endpoints to interact with the MySQL database:

- `GET /budget_items` Fetches all budget items.
- `GET /records` Fetches all records.
- `POST /budget_items` Adds a new budget item.

The server code is in the server.js file:

## SQL

In the Budget Tracker project, a MySQL database was used to store and manage budget items. The SQL commands used in creating the database, tables, and inserting records are as follows:

### Database Creation

To create a database, the `CREATE DATABASE` command is used:

```sql 
CREATE DATABASE budget_tracker;
```

### Table Creation

The `CREATE TABLE` command is used to create a new table in the database. In this project, a table named budget_items is created to store the budget items.

```sql
CREATE TABLE budget_items (
    id INT AUTO_INCREMENT PRIMARY KEY,
    type VARCHAR(20) NOT NULL,
    category VARCHAR(50) NOT NULL,
    note TEXT,
    amount DECIMAL(10, 2) NOT NULL,
    date DATE
);
```

In this table:

•	id is the primary key, which uniquely identifies each record.
•	type stores the type of the budget item (income or expense).
•	category stores the category of the budget item.
•	note stores any notes related to the budget item.
•	amount stores the amount of the budget item.
•	date stores the date of the budget item.

### Inserting Records

The `INSERT INTO` command is used to insert new records into a table:

```sql
INSERT INTO budget_items (type, category, note, amount, date) 
VALUES ('income', 'job', 'Salary for the month of January', 5000.00, '2023-01-31');
```

This command inserts a new income item into the budget_items table.

### Fetching Records
The `SELECT` command is used to fetch records from a table:

```sql
SELECT * FROM budget_items;
```


This command fetches all records from the budget_items table.

## Installation

### Prerequisites

Before you can use the Budget Tracker, you need to have the following installed on your computer:

•	NodeJS
•	Xampp

### Setting up the Database

Before running the application, you need to set up the MySQL database. Follow these steps:

1.	Start your Xampp server.
2.	Open your web browser and navigate to http://localhost/phpmyadmin.
3.	Click on the "Databases" tab and create a new database named budget_tracker.
4.	Select the budget_tracker database and click on the "SQL" tab.
5.	Paste the following SQL commands into the text box:

```sql
CREATE TABLE budget_items (
    id INT AUTO_INCREMENT PRIMARY KEY,
    type VARCHAR(20) NOT NULL,
    category VARCHAR(50) NOT NULL,
    note TEXT,
    amount DECIMAL(10, 2) NOT NULL,
    date DATE
);
```

6.	Click on the "Go" button to execute the commands.

### Setting up the Project

To install the Budget Tracker, follow these steps:

1.	Clone the repository:
```bash
git clone https://github.com/dimaliwatkent/budget-tracker.git
```

2.	Navigate into the project directory:

```bash
cd budget-tracker
```

3.	Install the necessary dependencies:

```bash
npm install
```

4.	Run the project:

```bash
npm start
```

## Usage

Video Demo Link
[Google Drive Video](https://drive.google.com/file/d/10JRMoI4ZX3EBMMfgSaF3b09pknc-B-XC/view?usp=sharing)

### Contributors

- **Zedrick Ragas**

    - Responsible for the front-end development of the Budget Tracker application. This included designing and implementing the user interface, writing the HTML, CSS, and JavaScript code that powers the interface, and ensuring that the application is responsive and user-friendly.

- **Kent Diether Dimaliwat**

    - Handled the back-end development of the application. He wrote the server code using Node.js and Express, set up the endpoints for fetching and adding budget items, and ensured that the server communicates effectively with the front-end of the application.

- **Vienna Piguerra**

    - In charge of all database-related tasks. She wrote the SQL commands for creating the database, tables, and columns, and for inserting and fetching data. Her work was key to ensuring that the application can store and manage budget items effectively.
