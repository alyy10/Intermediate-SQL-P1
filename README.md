# Intermediate SQL Project: Employee and Department Management Part 01

This repository contains the implementation of a comprehensive **Database Management System** using SQL, focusing on **Data Definition Language (DDL)** operations and **Data Analysis** techniques. The system allows for the creation, management, and analysis of employee, department, job, and location data for a fictional company.

## Overview

This project aims to demonstrate an efficient way to manage and analyze company data, leveraging SQL for defining tables, relationships, and performing data analysis. The data includes employees, their departments, job history, locations, and the regions they belong to.

## Key Features

- **Data Definition Language (DDL)**:
  - **Create**: Defines tables for regions, countries, locations, departments, jobs, employees, and job history.
  - **Alter**: Allows modifications to existing tables (e.g., adding new columns, foreign keys).
  - **Insert**: Inserts data into tables for regions, countries, departments, jobs, and employees.

- **Data Analysis**:
  - Various SQL join techniques, including:
    - **INNER JOIN**
    - **LEFT OUTER JOIN**
    - **RIGHT OUTER JOIN**
    - **FULL OUTER JOIN**
    - **SELF JOIN**
  - **UNION** and **UNION ALL** operations for combining datasets.
  - **INTERSECT** and **MINUS** for comparing data across tables.
  
- **Advanced SQL**:
  - Procedures and triggers for securing data modification during business hours.
  - Job history tracking via triggers for employee job changes.
  - Complex relationships across tables with foreign keys to ensure data integrity.

## Tables and Their Purpose

### 1. **Regions Table**
   Stores region information and has a one-to-many relationship with the `Countries` table.

### 2. **Countries Table**
   Contains country details and a reference to the `Regions` table.

### 3. **Locations Table**
   Stores location addresses for company departments, with a foreign key referencing the `Countries` table.

### 4. **Departments Table**
   Contains department names and references both the `Locations` and `Employees` tables.

### 5. **Jobs Table**
   Defines job titles and salary ranges, with a reference to the `Employees` table.

### 6. **Employees Table**
   Holds employee information, including personal details, job, and department associations. Self-referencing foreign keys track managers.

### 7. **Job History Table**
   Keeps track of the changes in job roles for employees, with references to the `Jobs`, `Departments`, and `Employees` tables.

### 8. **Employee Details View**
   A view combining employee, job, department, location, country, and region data to present a comprehensive employee profile.

## SQL Operations

### 1. **DDL Operations**
   - **CREATE**: Defines the tables with proper relationships and constraints (primary keys, foreign keys).
   - **ALTER**: Modifies existing tables (e.g., adding new columns).
   - **INSERT**: Adds sample data to the tables to simulate real-world data.
   - **Sequences**: Automatically generate unique IDs for tables like `Employees` and `Departments`.

### 2. **Data Analysis Queries**
   - **Joins**:
     - Combine data from multiple tables based on related keys.
     - Retrieve employee, department, job, and location information using inner and outer joins.
   - **Set Operations**:
     - **UNION** and **UNION ALL** to merge datasets.
     - **INTERSECT** to find common data across tables.
     - **MINUS** to find missing data in tables.
   
### 3. **Procedures and Triggers**
   - **Triggers**: Implemented to automatically log job history whenever an employee's job or department is updated.
   
