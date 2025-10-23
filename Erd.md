STUDENTS ||--o{ ENROLLMENT }o--|| COURSES

STUDENTS:
- student_id (PK)
- first_name
- last_name
- email (UNIQUE)
- gender
- created_at

COURSES:
- course_id (PK)
- course_name
- credits

ENROLLMENT:
- enrollment_id (PK)
- student_id (FK → students.student_id)
- course_id (FK → courses.course_id)
- enrollment_date

- ┌─────────────────┐                ┌─────────────────┐                ┌─────────────────┐
│    STUDENTS     │                │   ENROLLMENT    │                │     COURSES     │
├─────────────────┤                ├─────────────────┤                ├─────────────────┤
│ student_id (PK) │◄───────────────┤ enrollment_id(PK)│──────────────►│ course_id (PK)  │
│ first_name      │                │ student_id (FK) │                │ course_name     │
│ last_name       │                │ course_id (FK)  │                │ credits         │
│ email (UQ)      │                │ enrollment_date │                │                 │
│ gender          │                │                 │                │                 │
│ created_at      │                │                 │                │                 │
└─────────────────┘                └─────────────────┘                └─────────────────┘


Relationship Details

1. Students to Enrollment (One-to-Many)

Cardinality: 1:N

Description: One student can enroll in many courses.

Foreign Key: enrollment.student_id → students.student_id

Delete Rule: CASCADE

2. Courses to Enrollment (One-to-Many)

Cardinality: 1:N

Description: One course can have many students enrolled.

Foreign Key: enrollment.course_id → courses.course_id

Delete Rule: CASCADE

Business Rules

Students must have unique email addresses.

Courses must have a positive credit value.

Enrollments cannot exist without valid student and course references.

A student cannot be enrolled in the same course more than once.

Enrollment date records when a student joined a course.

Views and Derived Data

student_course_summary View:

Joins all three tables to show which students are enrolled in which courses.

Includes total courses per student and total students per course.

✅ This ERD demonstrates:
3 Tables: Students, Courses, Enrollment

Foreign Key Relationships: student_id, course_id

Many-to-Many Relationship: Between Students and Courses through Enrollment

Normalization & Referential Integrity maintained.
