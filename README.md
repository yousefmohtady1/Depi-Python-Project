# Employee Data Management System

A simple Python-based command-line application to manage employee records using CSV file storage.

## Project Description

This project is designed to manage employee information through a basic CLI (Command Line Interface).  
It demonstrates core Python concepts such as:

- Object-Oriented Programming (OOP)
- Dictionaries and Lists
- File Handling using the `csv` module
- Functions and Conditional Logic
- Error Handling and Data Validation

## Features

- **Add Employee**
- **View All Employees**
- **Update Employee**
- **Delete Employee**
- **Search Employee**
- **Exit Program**

Each employee has the following fields:

- `ID`
- `Name`
- `Position`
- `Salary`
- `Email`

## How It Works

1. When the program starts, it loads employee data from `employees.csv` (if it exists).
2. A menu is displayed for the user to interact with the system.
3. Any changes (add/update/delete) are immediately saved to the CSV file.
4. Data is persistent across program runs.

## File Structure

```
employee_data_manager/
│
├── employees.csv           # Employee data (auto-generated if not found)
├── employeeManager.ipynb   # Main application code
└── README.md               # Project documentation (this file)
```

## Validation & Error Handling

- Prevents duplicate employee IDs
- Validates that the salary is a numeric value
- Validates that the email is a valid email
- Checks if records exist before attempting to list, update, or delete
- Displays formatted output for better readability

## How to Run

```bash
python employee_manager.py
```

## Author

- Yosef Mohtady
- GitHub: [yousefmohtady1]

---
