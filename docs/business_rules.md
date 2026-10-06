# University Course Database - Business Rules

## Business Rules

1. A department can offer many courses, but each course belongs to one department.
   - Relationship: Department to Course
   - Cardinality: One-to-Many (1:M)
   - Participation: Each Course must belong to a Department.

2. A department can have many instructors, but each instructor belongs to one department.
   - Relationship: Department to Instructor
   - Cardinality: One-to-Many (1:M)
   - Participation: Each Instructor must belong to a Department.

3. A course can have many sections, but each section is associated with one course.
   - Relationship: Course to Section
   - Cardinality: One-to-Many (1:M)
   - Participation: Each Section must be associated with a Course.

4. An instructor can teach many sections, but each section is taught by one instructor.
   - Relationship: Instructor to Section
   - Cardinality: One-to-Many (1:M)
   - Participation: Each Section must have an Instructor.

5. A semester can contain many sections, but each section occurs during one semester.
   - Relationship: Semester to Section
   - Cardinality: One-to-Many (1:M)
   - Participation: Each Section must belong to a Semester.

6. A student can have many enrollment records, but each enrollment record belongs to one student.
   - Relationship: Student to Enrollment
   - Cardinality: One-to-Many (1:M)
   - Participation: Each Enrollment must have a Student.

7. A section can have many enrollment records, but each enrollment record belongs to one section.
   - Relationship: Section to Enrollment
   - Cardinality: One-to-Many (1:M)
   - Participation: Each Enrollment must belong to a Section.

8. Students and sections have a many-to-many relationship that is resolved through the Enrollment entity.
   - Relationship: Student to Section
   - Cardinality: Many-to-Many (M:N)
   - Associative Entity: Enrollment
