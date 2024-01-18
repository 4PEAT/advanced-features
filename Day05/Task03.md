### Task: Implement a Student Grading System using a Map in Java

#### Scenario
You are developing a simple grading system for a classroom. This system will store students' names and their corresponding grades. Your task is to create a Java program that uses a `Map` to manage this information.

#### Task Description
1. **Create a Student-Grade Map**:
   - Use a suitable `Map` implementation in Java (like `HashMap`) to store student names as keys and their grades as values. The student names are strings and the grades can be represented as integers or floats.

2. **Add Student Grades to the Map**:
   - Implement a method to add a new student's name and grade to the map. Ensure that no duplicate student names are added.

3. **Update Grades**:
   - Implement a method to update the grade for an existing student. This method should check if the student exists before updating the grade.

4. **Retrieve a Grade**:
   - Implement a method to retrieve a student's grade by their name.

5. **Print All Grades**:
   - Implement a method to print out all student names and their grades.

6. **Handle Invalid Operations**:
   - Ensure your program gracefully handles scenarios like trying to retrieve or update a grade for a student who is not in the map.

#### Example Use Cases
- Adding students "Alice" with grade 90, "Bob" with grade 85, and "Charlie" with grade 92.
- Updating the grade for "Alice" to 95.
- Retrieving and printing the grade for "Bob".
- Printing all student grades.

This task requires you to apply basic Map operations in Java and is a good exercise to understand how to store and manipulate key-value pairs. It also involves some error handling for non-existing keys.
