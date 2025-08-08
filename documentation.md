# Employee Management System Documentation

## Overview
The Employee Management System is a Python-based application designed to manage employee records. It provides functionalities to add, update, delete, search, and list employee information, with data persistence using a CSV file.

## Table of Contents
- [Features](#features)
- [System Requirements](#system-requirements)
- [File Structure](#file-structure)
- [Class and Methods](#class-and-methods)
- [Validation Functions](#validation-functions)
- [Usage](#usage)
- [Error Handling](#error-handling)

## Features
- **Add Employee**: Add a new employee with details such as ID, name, position, salary, and email.
- **Update Employee**: Modify existing employee details by ID.
- **Delete Employee**: Remove an employee record by ID.
- **Search Employee**: Retrieve and display details of an employee by ID.
- **List Employees**: Display all employee records in a formatted table.
- **Data Persistence**: Store employee data in a CSV file (`employees.csv`) for persistence.
- **Input Validation**: Ensure valid numeric input for ID and salary, and valid email format.

## System Requirements
- Python 3.x
- Standard Python libraries: `csv`, `re`
- No external dependencies required

## File Structure
- **employees.csv**: Stores employee data with columns `Id`, `Name`, `Position`, `Salary`, and `Email`.
- **main.py**: The main Python script containing the `EmployeeManager` class and program logic.

## Class and Methods
### `EmployeeManager` Class
Manages employee data with the following attributes and methods:

#### Attributes
- `__employees`: Private dictionary storing employee data with ID as the key.
- `__FileName`: Private string specifying the CSV file name (`employees.csv`).

#### Methods
- `__init__()`: Initializes the employee dictionary and loads data from the CSV file.
- `GetEmployee()`: Returns the employee dictionary.
- `__LoadData()`: Loads employee data from `employees.csv` into the dictionary. Handles `FileNotFoundError` gracefully.
- `SaveData()`: Saves the employee dictionary to `employees.csv`.
- `AddEmployee(empId, name, position, salary, email)`: Adds a new employee if the ID is unique.
- `UpdateEmployee(empId, name=None, position=None, salary=None, email=None)`: Updates an existing employee's details by ID.
- `DeleteEmployee(empId)`: Deletes an employee by ID.
- `SearchEmployee(empId)`: Returns employee details by ID or `None` if not found.
- `ListEmployee()`: Displays all employees in a formatted table.
- `ExitEmployee()`: Prints a goodbye message and exits the program.

## Validation Functions
- `ValidateNumeric(prompt)`: Ensures the input is a numeric value (used for ID and salary).
- `ValidateEmail(prompt)`: Validates email format using a regular expression (`^[\w\.-]+@[\w\.-]+\.\w+$`).

## Usage
1. Run the script to start the Employee Management System.
2. Choose from the following menu options:
   - **1: View all employees**: Displays all employee records in a table.
   - **2: Add employee**: Prompts for ID, name, position, salary, and email, then adds the employee.
   - **3: Update employee**: Prompts for ID and new details to update an existing employee.
   - **4: Delete employee**: Prompts for ID to delete an employee.
   - **5: Search employee**: Prompts for ID to display an employee's details.
   - **6: Exit**: Exits the program.
3. Input validation ensures correct data entry for ID, salary, and email.

### Example Workflow
```
Welcome To Employees Management System
----------------------------------------
1- View all employees
2- Add employee
3- Update employee
4- Delete employee
5- Search employee
6- Exit
Enter your choice: 2
Enter employee ID: 1
Enter employee name: John Doe
Enter employee position: Developer
Enter employee salary: 50000
Enter employee Email: john.doe@example.com
Employee added successfully
```

## Error Handling
- **FileNotFoundError**: Handled during CSV file loading to allow the program to start even if `employees.csv` does not exist.
- **Duplicate ID**: Prevents adding an employee with an existing ID.
- **Invalid Input**: Ensures numeric inputs for ID and salary, and valid email format.
- **Non-existent Employee**: Displays appropriate messages when updating, deleting, or searching for an employee that does not exist.