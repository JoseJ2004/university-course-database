# Logical Database Schema
Name: Jose Joao
Date: 10/06/2026

## 1. Departments
- department_id INT PRIMARY KEY
- department_name VARCHAR(100) NOT NULL UNIQUE

## 2. Students
- student_id INT PRIMARY KEY
- first_name VARCHAR(100) NOT NULL
- last_name VARCHAR(100) NOT NULL
- email VARCHAR(255) NOT NULL UNIQUE

## 3. Instructors
- instructor_id INT PRIMARY KEY
- first_name VARCHAR(100) NOT NULL
- last_name VARCHAR(100) NOT NULL
- email VARCHAR(255) NOT NULL UNIQUE
- department_id INT NOT NULL, FOREIGN KEY references Departments(department_id)

## 4. Courses
- course_id INT PRIMARY KEY
- course_name VARCHAR(150) NOT NULL
- credits INT NOT NULL
- department_id INT NOT NULL, FOREIGN KEY references Departments(department_id)
- instructor_id INT NOT NULL, FOREIGN KEY references Instructors(instructor_id)

## 5. Enrollments
- enrollment_id INT PRIMARY KEY
- student_id INT NOT NULL, FOREIGN KEY references Students(student_id)
- course_id INT NOT NULL, FOREIGN KEY references Courses(course_id)
- enrollment_date DATE NOT NULL
- semester VARCHAR(30) NOT NULL
- grade VARCHAR(2) NULL
- UNIQUE (student_id, course_id, semester)

## Relationships
- One department has many instructors.
- One department offers many courses.
- One instructor teaches many courses.
- One student has many enrollments.
- One course has many enrollments.
- Enrollments connects Students and Courses in a many-to-many relationship.

