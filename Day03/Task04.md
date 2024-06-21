
#### Exercise: Developing a Student Grade Management System with Exception Handling

#### Objective:
The objective of this exercise is to understand and apply Java exception handling mechanisms. You will learn how to throw, catch, and handle different types of exceptions in a student grade management context.

#### Description:
You are tasked with creating a student grade management system that supports adding students, recording grades, and calculating grade point averages (GPA). The system should handle various exceptions that might occur during these operations.

#### Classes to Implement:

1. **Student**:
   - **Attributes**:
     - `String studentId`
     - `String name`
     - `List<Double> grades`
   - **Methods**:
     - Constructor to initialize the student with an ID, name, and an empty list of grades.
     - `void addGrade(double grade) throws InvalidGradeException`: Method to add a grade to the student's record.
     - `double calculateGPA() throws NoGradesException`: Method to calculate the student's GPA.
     - `String toString()`: Method to return a string representation of the student.

2. **InvalidGradeException** (Custom Exception):
   - **Attributes**:
     - `double grade`
   - **Methods**:
     - Constructor to initialize the exception with the invalid grade.
     - `double getGrade()`: Method to return the invalid grade.
     - `String toString()`: Method to return a string representation of the exception.

3. **NoGradesException** (Custom Exception):
   - **Methods**:
     - Constructor to initialize the exception with a default message.
     - `String toString()`: Method to return a string representation of the exception.

4. **GradeManagementSystem**:
   - **Attributes**:
     - `List<Student> students`
   - **Methods**:
     - Constructor to initialize the system with an empty list of students.
     - `void addStudent(Student student)`: Method to add a student to the system.
     - `Student getStudentById(String studentId) throws StudentNotFoundException`: Method to retrieve a student by ID.
     - `void displayAllStudents()`: Method to display details of all students.

5. **StudentNotFoundException** (Custom Exception):
   - **Attributes**:
     - `String studentId`
   - **Methods**:
     - Constructor to initialize the exception with the student ID that was not found.
     - `String getStudentId()`: Method to return the student ID that was not found.
     - `String toString()`: Method to return a string representation of the exception.

6. **Main**:
   - **Methods**:
     - `main(String[] args)`: Method to test the functionality of the student grade management system, including exception handling.

#### Task:

1. **Define the Student Class**:
   - Create the `Student` class with the specified attributes (`studentId`, `name`, `grades`).
   - Implement a constructor to initialize the student with an ID, name, and an empty list of grades.
   - Implement the `addGrade` method to add a grade to the student's record. If the grade is less than 0.0 or greater than 4.0, throw an `InvalidGradeException` with the invalid grade.
   - Implement the `calculateGPA` method to calculate the student's GPA. If the student has no grades recorded, throw a `NoGradesException`.
   - Implement the `toString` method to return a string representation of the student.

2. **Define the InvalidGradeException Class**:
   - Create the `InvalidGradeException` class with the specified attributes (`grade`).
   - Implement a constructor to initialize the exception with the invalid grade.
   - Implement the `getGrade` method to return the invalid grade.
   - Implement the `toString` method to return a string representation of the exception.

3. **Define the NoGradesException Class**:
   - Create the `NoGradesException` class.
   - Implement a constructor to initialize the exception with a default message.
   - Implement the `toString` method to return a string representation of the exception.

4. **Define the GradeManagementSystem Class**:
   - Create the `GradeManagementSystem` class with the specified attributes (`students`).
   - Implement a constructor to initialize the system with an empty list of students.
   - Implement the `addStudent` method to add a student to the system.
   - Implement the `getStudentById` method to retrieve a student by ID. If the student ID is not found, throw a `StudentNotFoundException` with the student ID.
   - Implement the `displayAllStudents` method to display details of all students.

5. **Define the StudentNotFoundException Class**:
   - Create the `StudentNotFoundException` class with the specified attributes (`studentId`).
   - Implement a constructor to initialize the exception with the student ID that was not found.
   - Implement the `getStudentId` method to return the student ID that was not found.
   - Implement the `toString` method to return a string representation of the exception.

6. **Main Class**:
   - Write a `Main` class to test the functionality of the student grade management system.
   - Create instances of `Student`, `InvalidGradeException`, `NoGradesException`, and `StudentNotFoundException`.
   - Add students to the grade management system.
   - Add grades to students and handle exceptions if the grades are invalid.
   - Calculate GPA for students and handle exceptions if no grades are recorded.
   - Retrieve students by ID and handle exceptions if the student ID is not found.
   - Display details of all students to ensure the system works as expected.
