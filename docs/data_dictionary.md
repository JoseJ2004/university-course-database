
# Data Dictionary
Name: Jose Joao
Date: 10/06/2026

## DEPARTMENTS
| Column | Type | Key | Null | Description |
|---|---|---|---|---|
| department_id | INT | PK | No | Unique department ID |
| department_name | VARCHAR(100) | UNIQUE | No | Department name |

## STUDENTS
| Column | Type | Key | Null | Description |
|---|---|---|---|---|
| student_id | INT | PK | No | Unique student ID |
| first_name | VARCHAR(100) | | No | Student first name |
| last_name | VARCHAR(100) | | No | Student last name |
| email | VARCHAR(255) | UNIQUE | No | Student email |

## INSTRUCTORS
| Column | Type | Key | Null | Description |
|---|---|---|---|---|
| instructor_id | INT | PK | No | Unique instructor ID |
| first_name | VARCHAR(100) | | No | Instructor first name |
| last_name | VARCHAR(100) | | No | Instructor last name |
| email | VARCHAR(255) | UNIQUE | No | Instructor email |
| department_id | INT | FK | No | References Departments |

## COURSES
| Column | Type | Key | Null | Description |
|---|---|---|---|---|
| course_id | INT | PK | No | Unique course ID |
| course_name | VARCHAR(150) | | No | Course title |
| credits | INT | | No | Number of credits |
| department_id | INT | FK | No | References Departments |
| instructor_id | INT | FK | No | References Instructors |

## ENROLLMENTS
| Column | Type | Key | Null | Description |
|---|---|---|---|---|
| enrollment_id | INT | PK | No | Unique enrollment ID |
| student_id | INT | FK | No | References Students |
| course_id | INT | FK | No | References Courses |
| enrollment_date | DATE | | No | Enrollment date |
| semester | VARCHAR(30) | | No | Academic semester |
| grade | VARCHAR(2) | | Yes | Student grade |

## Additional Constraint
UNIQUE(student_id, course_id, semester)
prevents duplicate enrollment in the same course
during the same semester.

