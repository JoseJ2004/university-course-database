# University Course Registration Database

## Problem Description

Universities need to manage large amounts of information about students, courses, instructors, departments, and course enrollments. When this information is stored manually or across separate files, it can lead to duplicated data, errors, and difficulty retrieving important information.

This project will create a centralized database to organize university course registration information and make it easier to manage students, courses, instructors, departments, and enrollments.

## Purpose of the Database

The purpose of the database is to provide a structured system for storing and managing university course registration information.

The database will allow users to track students, courses, instructors, departments, and enrollments. It will also support queries that help users retrieve academic and registration information efficiently.

## Intended Users

The intended users include:

- University administrators
- Registration office staff
- Academic staff
- Instructors
- Students

## Major Data That Must Be Stored

The database will store information about:

### Students
- Student ID
- First name
- Last name
- Email
- Date of birth
- Major

### Courses
- Course ID
- Course name
- Course description
- Number of credits
- Department

### Instructors
- Instructor ID
- First name
- Last name
- Email
- Department

### Departments
- Department ID
- Department name

### Enrollments
- Enrollment ID
- Student ID
- Course ID
- Enrollment date
- Semester
- Grade

## Questions the Database Should Eventually Answer

1. Which courses is a particular student enrolled in?
2. Which students are enrolled in a particular course?
3. Which instructor teaches a particular course?
4. How many students are enrolled in each course?
5. Which courses belong to a particular department?
6. What grades has a student received in completed courses?
7. Which courses are taught by a particular instructor?
8. How many courses is each student taking during a particular semester?

## Initial Business Rules

1. Each student must have a unique student ID.
2. Each course must have a unique course ID.
3. Each instructor must have a unique instructor ID.
4. Each department must have a unique department ID.
5. A student can enroll in multiple courses, and a course can have multiple students.
6. Each enrollment must be associated with exactly one student and one course.
7. Each course belongs to one department, while a department can offer multiple courses.
8. Each instructor belongs to one department, while a department can have multiple instructors.
9. An instructor can teach multiple courses.
10. A student cannot be enrolled in the same course more than once during the same semester.
