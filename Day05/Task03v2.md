

# Task: Implement an Advanced Student Grading System Using a Map in Java

## Scenario
You are tasked with building a **student grading system** for a classroom environment.  
This system must efficiently store and manage student information, including **multiple grades** per student. The goal is to practice **Map operations**, **object-oriented programming**, and basic **data processing** techniques in Java.

---

## Task Description

### 1. Define the `Student` Class:
- Create a `Student` class with at least the following attributes:
  - `id` (int) – unique identifier for each student
  - `name` (String) – student's full name
- Override `equals()` and `hashCode()` based on `id` to ensure correct behavior when used as Map keys.
- Implement `toString()` for easy display of student information.

### 2. Create the Student-Grades Map:
- Use a suitable Map implementation (`HashMap` recommended) to store:
  - **Key**: `Student` object
  - **Value**: a `List<Integer>` representing all the grades the student received.

Example:  
```java
Map<Student, List<Integer>> studentGrades = new HashMap<>();
```

### 3. Core Functionalities:

#### a) Add a New Student
- Implement a method to add a new student with an empty list of grades.
- Prevent duplicate students based on `id`.

#### b) Add Grades
- Implement a method to add a grade to an existing student's list of grades.
- Validate that the student exists before adding the grade.

#### c) Update Grades (Optional)
- Implement a method to update the most recent grade of a student.

#### d) Retrieve Student Grades
- Implement a method to retrieve all grades for a given student by `id`.
- If the student does not exist, display a friendly error message.

#### e) Calculate Average Grade
- Implement a method to calculate and return the average grade for a student.

#### f) Print All Students and Grades
- Display each student’s name, ID, all grades, and their average grade.
- Optionally, allow printing sorted by name or average grade.

---

## 4. Exception and Edge Case Handling:
- Handle scenarios gracefully, such as:
  - Adding a grade for a non-existent student.
  - Calculating an average for a student with no grades.
  - Attempting to add a duplicate student.

---

## 5. Additional Challenges (Optional, for Extra Difficulty):
- Support removing students from the system.
- Save the student-grade database to a text file (e.g., CSV format).
- Load existing student data from a file when the program starts.
- Support multiple classes/courses (e.g., Math, Science) for each student.
- Simulate a login system where only authorized users can modify grades.

---

## Example Use Cases
- Add students: "Alice" (ID 1), "Bob" (ID 2), "Charlie" (ID 3).
- Add multiple grades for each student.
- Update Alice’s last grade.
- Retrieve and print Bob’s grades and average.
- Print all students sorted alphabetically.
- Remove a student and verify the update.

---

# Learning Objectives
- Master basic and advanced usage of `Map` and `List` in Java.
- Understand the importance of properly overriding `equals()` and `hashCode()`.
- Practice working with collections of objects and data aggregation.
- Improve skills in exception handling and defensive programming.
