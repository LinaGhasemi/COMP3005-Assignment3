# COMP 3005 - Assignment 3: Student Management System

## Database Setup

1. Open pgAdmin 4 and connect to your PostgreSQL server.
2. Create a database named `Student Management System`.
3. Open the Query Tool for the new database.
4. Open and execute the `database/setup.sql` file.

The SQL script creates the `students` table and inserts three initial student records.

## Application Setup

1. Open the project folder in VS Code and open a PowerShell terminal.

2. Create a Python virtual environment:

   ```powershell
   py -m venv .venv
   ```

3. Install the required dependencies:

   ```powershell
   .venv\Scripts\python.exe -m pip install -r requirements.txt
   ```

4. Set your PostgreSQL password:

   ```powershell
   $env:DB_PASSWORD = Read-Host "Enter PostgreSQL password"
   ```

   The application uses these default connection settings:

   - Host: `localhost`
   - Port: `5432`
   - Database: `Student Management System`
   - Username: `postgres`

   If necessary, the `DB_HOST`, `DB_PORT`, and `DB_USER` environment variables can be used to change the connection settings.

5. Run the Python application:

   ```powershell
   .venv\Scripts\python.exe application\main.py
   ```

6. Follow the terminal menu to perform the four CRUD operations.

## CRUD Functions

The application implements the following four functions:

- **getAllStudents():** Retrieves and displays all student records from the database.
- **addStudent(first_name, last_name, email, enrollment_date):** Adds a new student to the database.
- **updateStudentEmail(student_id, new_email):** Updates the email address of an existing student.
- **deleteStudent(student_id):** Deletes a student record using its student ID.

## Demonstration Video

Video link: https://youtu.be/62C9SVjU4-8