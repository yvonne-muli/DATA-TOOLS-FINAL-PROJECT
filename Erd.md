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
