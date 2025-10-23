# DATA-TOOLS-FINAL-PROJECT
# My SCHOOL COURSE ENROLLMENT SQL PROJect

<a name="readme-top"></a>

<!-- TABLE OF CONTENTS -->

# 📗 Table of Contents

- [My SQL Project](#about-project)
- [📗 Table of Contents](#-table-of-contents)
- [📖 My SQL Project](#about-project)
  - [🛠 Built With ](#-built-with-)
    - [Tech Stack ](#tech-stack-)
    - [Key Features ](#key-features-)
  - [💻 Getting Started ](#-getting-started-)
    - [Prerequisites](#prerequisites)
    - [Setup](#setup)
    - [Usage](#usage)
  - [👥 Authors ](#-authors-)
  - [🔭 Future Features ](#-future-features-)
  - [🤝 Contributing ](#-contributing-)

<!-- PROJECT DESCRIPTION -->

# 📖 My SQL Project <a name="about-project"></a>

**My SQL Project** is a simple Database that uses SQL, Postgres via Supabase and R to create, query and secure a **SCHOOL** database.

## 🛠 Built With <a name="built-with"></a>

### Tech Stack <a name="tech-stack"></a>
- SQL
- Postgres DB

<!-- Features -->

### Key Features <a name="key-features"></a>

- [ ] **Tables**
- [ ] **Schema**
- [ ] **Access control**

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## 💻 Getting Started <a name="getting-started"></a>

To rebuild this DB, follow these steps

### Prerequisites

To run this project, you need:
- [A Supabase account](https://supabase.com/)
- [Knowledge on SQL](https://www.w3schools.com/sql/)
- A schema for creating your tables in the DB

<!-- ### Setup -->
### Setup

Copy the contents of this Readme.md to your Project's file

OR

Clone this repository to your desired folder:

```sh
  git clone https://github.com/joyapisi/readme-template-data
  cd budget-app
```

<!-- ### DB Creation -->

### DB Schema

- The DB is made up of 3 tables. Eaach table has 5 entries.
- To create the table, you will need a schema as shown below:

```sql
-- Drop old tables if they exist
DROP TABLE IF EXISTS Students CASCADE;
DROP TABLE IF EXISTS Courses CASCADE;
DROP TABLE IF EXISTS Enrollment CASCADE;


-- Create Students table
CREATE TABLE School.Students (
  student_id SERIAL PRIMARY KEY,
  first_name TEXT,
  last_name TEXT,
  email VARCHAR,
  gender TEXT
);

-- Create Courses table
CREATE TABLE School. courses (
    course_id INT PRIMARY KEY,
    course_name VARCHAR(100),
    credits INT
);

-- Create Enrollment table
CREATE TABLE School.Enrollment (
  enrollment_id SERIAL PRIMARY KEY,
  student_id INT,
  course_id INT 
);



-- Insert sample Students (5 rows)
INSERT INTO School.Students(student_id,first_name,last_name,email,gender)
values
(1,'Yvonne','Muli','muliyvonne@gmail.com','Female'),
(2,'John','Nganga','ngangajohn@gmail.com','Female'),
(3,'George','Mbugua','mbuguageorge@gmail.com','Female'),
(4,'Cate','Mwende','mwendecate@gmail.com','Female'),
(5,'Ann','Mueni','mueniann@gmail.com','Female');

-- Insert sample Courses (5 rows)
INSERT INTO courses (course_id, course_name, credits) VALUES
(1, 'Mathematics', 3),
(2, 'Physics', 4),
(3, 'Chemistry', 3),
(4, 'Biology', 2),
(5, 'Computer Science', 5);

-- Insert sample Enrollment (5 rows)
INSERT INTO Enrollment(enrollment_id,student_id,course_id)
VALUES 
(1,1,2),
(2,2,1),
(3,3,3)
(4,1,4),
(5,2,5);

```

- The Tables should look like this in Supabase:
- Students
<img width="1021" height="720" alt="image" src="https://github.com/user-attachments/assets/cbd1373e-fdd2-4ebb-9e4d-2fa7a3f14e85" />

Courses
<img width="627" height="737" alt="image" src="https://github.com/user-attachments/assets/82b8e355-0396-41ee-b001-dca7afb3cd27" />

Enrollment:
<img width="685" height="620" alt="image" src="https://github.com/user-attachments/assets/afe6aec0-593b-4cef-b942-4fc4d48d66fd" />


- The ERD screenshot from Supabase looks like this: 
<img width="588" height="866" alt="image" src="https://github.com/user-attachments/assets/7d5c55b5-194e-41b4-abbe-19e30f8fa6b8" />

- To test the table, I used two queries: 

```sql
SELECT *
FROM School.Students
WHERE first_name = 'Yvonne Muli'
````

```sql
SELECT * FROM 
WHERE = "TRUE"
````

- Here are the results of the queries:
<img width="774" height="365" alt="image" src="https://github.com/user-attachments/assets/d1e17598-f309-414e-a781-0ed8ea29530c" />


<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- AUTHORS -->

## 👥 Authors <a name="authors"></a>

👤 **Yvonne Muli**

- GitHub: [@yvonnemuli](https://github.com/yvonne-muli)
- LinkedIn: [@yvonne muli](https://linkedin.com/in/yvonne muli)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- FUTURE FEATURES -->

## 🔭 Future Features <a name="future-features"></a>

- [ ] **Add security**
- [ ] **Link DB to R for visualisation purposes and further analyses**

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## 🤝 Contributing <a name="contributing"></a>

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- SUPPORT -->
