## Online course
https://www.freecodecamp.org/learn/relational-database/learn-relational-databases-by-building-a-mario-database/build-a-mario-database
https://www.w3schools.com/mysql/mysql_rdbms.asp


### Signup/Register/Create Account
1. https://stackoverflow.com/users/signup
2. https://www.linkedin.com/signup
3. https://github.com/signup
4. https://chatgpt.com/

### Fill form
1. Skills: https://forms.gle/r6zQftWGtWZYNct78
2. 21 July 2024 RDBMS workshop form: https://forms.gle/Xij6fyAaXotot45R9

### What is an RDBMS?

A Relational Database Management System (RDBMS) is a type of database management system that stores data in a structured format using rows and columns. RDBMS uses SQL (Structured Query Language) for accessing and managing the data.

### Key Concepts in RDBMS

1. **Tables**: The primary structure that holds data. Each table consists of rows (records) and columns (attributes).
2. **Rows**: Individual records in a table.
3. **Columns**: Attributes or fields that define the data in the table.
4. **Primary Key**: A unique identifier for each row in a table.
5. **Foreign Key**: A column that creates a relationship between two tables.

### Example: Student Database

Let's create a simple student database to illustrate RDBMS concepts.

#### Tables

1. **Students**
    - `StudentID` (Primary Key)
    - `FirstName`
    - `LastName`
    - `DateOfBirth`
    - `MajorID` (Foreign Key)

2. **Majors**
    - `MajorID` (Primary Key)
    - `MajorName`

#### Sample Data

**Students Table**:
| StudentID | FirstName | LastName | DateOfBirth | MajorID |
|-----------|-----------|----------|-------------|---------|
| 1         | John      | Doe      | 2000-01-15  | 101     |
| 2         | Jane      | Smith    | 2001-03-22  | 102     |
| 3         | Alice     | Johnson  | 1999-12-30  | 101     |

**Majors Table**:
| MajorID | MajorName      |
|---------|-----------------|
| 101     | Computer Science|
| 102     | Mathematics     |

#### Relationships

- The `MajorID` in the `Students` table is a foreign key that references the `MajorID` in the `Majors` table. This creates a relationship between the two tables, indicating which major each student is enrolled in.

### SQL Queries

1. **Select all students**:
    ```sql
    SELECT * FROM Students;
    ```

2. **Select all majors**:
    ```sql
    SELECT * FROM Majors;
    ```

3. **Join Students with Majors to get student details with major names**:
    ```sql
    SELECT Students.StudentID, Students.FirstName, Students.LastName, Majors.MajorName
    FROM Students
    JOIN Majors ON Students.MajorID = Majors.MajorID;
    ```

#### Result of the Join Query:
| StudentID | FirstName | LastName | MajorName       |
|-----------|-----------|----------|-----------------|
| 1         | John      | Doe      | Computer Science|
| 2         | Jane      | Smith    | Mathematics     |
| 3         | Alice     | Johnson  | Computer Science|

### Explanation

- **Students Table**: Stores student information with a `StudentID` as the primary key.
- **Majors Table**: Stores major information with a `MajorID` as the primary key.
- **Foreign Key Relationship**: `Students.MajorID` references `Majors.MajorID`, linking students to their respective majors.
- **Join Query**: Combines data from `Students` and `Majors` tables based on the relationship, providing a comprehensive view of students and their majors.

This example demonstrates how RDBMS organizes data into related tables and uses SQL to manage and retrieve this data efficiently.
