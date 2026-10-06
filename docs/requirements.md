# University Course Database - Requirements

## Project Overview

The University Course Database is designed to organize information about students, courses, instructors, departments, and course enrollment.

## Entities

The database will contain the following entities:

1. Student
2. Course
3. Instructor
4. Department
5. Enrollment
6. Section
7. Semester

## Main Requirements

- The system stores student information.
- The system stores courses offered by the university.
- Each course belongs to a department.
- Instructors can teach course sections.
- Students can enroll in course sections.
- Enrollment records connect students to sections.
- Sections are offered during a specific semester.
- The system keeps information about university departments.

## Main Attributes

### Student
- Student_ID (Primary Key)
- First_Name
- Last_Name
- Email
- Major

### Course
- Course_ID (Primary Key)
- Course_Name
- Credits

### Instructor
- Instructor_ID (Primary Key)
- First_Name
- Last_Name
- Email

### Department
- Department_ID (Primary Key)
- Department_Name

### Enrollment
- Enrollment_ID (Primary Key)
- Enrollment_Date
- Grade

### Section
- Section_ID (Primary Key)
- Section_Number
- Room

### Semester
- Semester_ID (Primary Key)
- Semester_Name
- Year
