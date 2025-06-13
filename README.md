# 📊 Research Projects Database

This project is a relational database system designed to manage research projects, employees involved in those projects, and the funding agencies that support them. The system is implemented using SQL and captures core relationships and constraints typical in research institutions or R&D environments.

## 🧱 Features & Schema Overview

The database includes the following core entities:

- **Employee**: Contains details of employees including their SSN, name, and salary.
- **Funding Agency**: Stores information about agencies that fund research projects, including name and address.
- **Project**: Represents a research project with its name, duration, budget, and associated funding agency.
- **Project Manager**: A one-to-one relationship that maps each project to a manager, who is also an employee.
- **Employee_Project**: A junction table capturing which employees are assigned to which projects, and includes the manager overseeing each project.

## 🗃️ SQL Table Definitions

The schema is implemented using the following tables:

- `Employee`
- `FundingAgency`
- `Project`
- `Project_Manager`
- `Employee_Project`

Each table includes appropriate primary and foreign keys to maintain referential integrity.

## 🔗 Relationships

- Each **project** is funded by **one funding agency**.
- **Employees** can work on **multiple projects** (many-to-many relationship via `Employee_Project`).
- Each **project** has **exactly one manager**, who is also stored in the `Employee` table.
- Project names are **unique within a funding agency** (enforced logically, can be extended with constraints if needed).

## 📥 Sample Data

The database is populated with sample data for:
- 3 employees
- 3 funding agencies
- 3 projects
- 3 project managers (each managing and participating in a project)

## 📌 Assumptions

- Duration is stored in months (can be adjusted based on requirements).
- A manager is always an employee.
- An employee can manage and simultaneously work on the same project.

## 🛠️ Technologies Used

- SQL (DDL and DML)
- Relational Database Concepts (ER modeling)
- Designed for compatibility with PostgreSQL, MySQL, or any standard RDBMS.

## 📂 How to Use

1. Clone the repository.
2. Run the SQL scripts using your preferred SQL database engine.
3. Explore and modify the schema or data as needed.

---

🔍 Feel free to fork this project and expand it with advanced features such as:
- Project timelines
- Project deliverables
- Employee roles per project
- Agency-specific funding limits



![image](https://github.com/user-attachments/assets/2721d122-0608-465c-8932-d0c987d58673)

![image](https://github.com/user-attachments/assets/f59c0965-1ceb-48d3-b0e3-c2aa411a86d6)

