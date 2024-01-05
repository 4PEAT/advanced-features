Exercise: Employee Management System with Abstract Classes
Background:
In a company, there are various types of employees, such as salaried employees, hourly employees, and contract-based employees. Each type of employee has a different way of calculating their paycheck. The company wants to create an employee management system that can handle different types of employees and calculate their paychecks accordingly.

Objective:
Design and implement an employee management system using abstract classes and methods to handle different types of employees and calculate their paychecks.

Tasks:

Create an Abstract Class Employee:

Define an abstract class named Employee.
Add common properties that all employees share, such as name, id, and department.
Declare an abstract method double calculatePaycheck(): to calculate the paycheck of the employee.
Implement Concrete Subclasses:

Create a concrete subclass of Employee called SalariedEmployee. It should have:
A private instance variable for the annual salary.
A constructor to set the common properties and the annual salary.
An implementation for the calculatePaycheck() method, assuming bi-weekly pay periods.
Create a concrete subclass of Employee called HourlyEmployee. It should have:
Private instance variables for the hourly wage and hours worked.
A constructor to set the common properties, hourly wage, and hours worked.
An implementation for the calculatePaycheck() method.
Create a concrete subclass of Employee called ContractEmployee. It should have:
Private instance variables for the contract amount and the duration of the contract in months.
A constructor to set the common properties, contract amount, and duration.
An implementation for the calculatePaycheck() method, assuming monthly payments.
Implement an Employee Management Class:

Create a class EmployeeManager with a main method.
Instantiate several employees of different types and add them to an ArrayList<Employee>.
Iterate through the list and print out the details of each employee, including their calculated paycheck.
Bonus Challenges:

Implement a method void giveRaise(double percentage) in the Employee class that increases the employee's salary by a certain percentage. Then, override this method in each of the subclasses to adjust their specific pay attributes.
Add a method to the EmployeeManager class to calculate the total payroll of all employees and print the result.
