
---

# 1. Abstract Classes and Interfaces
Which statement correctly differentiates abstract classes from interfaces in Java?

A) Abstract classes can have multiple methods, but interfaces can only have one.  
B) Interfaces can have default methods with implementations, whereas abstract classes cannot.  
C) Abstract classes can have constructor methods, but interfaces cannot.  
D) Only abstract classes can have public methods.

---

# 2. Polymorphism
What is the output of the following Java code?
```java
class A {
    String show() { return "A"; }
}
class B extends A {
    String show() { return "B"; }
}
public class Test {
    public static void main(String args[]) {
        A obj = new B();
        System.out.println(obj.show());
    }
}
```
A) A  
B) B  
C) Compilation Error  
D) Runtime Error

---

# 3. Enumerations
Which of these is a valid use of an enumeration in Java?

A) To define a set of constants representing days of the week.  
B) To create a collection of objects.  
C) To declare a method within a class.  
D) To initialize thread states.

---

# 4. Generic Types
What does the following Java generic class definition specify?
```java
public class Box<T extends Number> { ... }
```
A) The Box class can only hold objects of type Number.  
B) The Box class can hold any type of object.  
C) The Box class can hold objects of Number type or its subclasses.  
D) The Box class is a type of Number.

---

# 5. Collections
In Java Collections Framework, which of the following is true about ArrayList and LinkedList?

A) ArrayList and LinkedList both use a dynamic array to store elements.  
B) ArrayList provides faster insertion and removal operations than LinkedList.  
C) LinkedList provides faster random access of elements than ArrayList.  
D) LinkedList consumes less memory than ArrayList for large lists.

---

# 6. Inner Classes
What is a characteristic of a static inner class in Java?

A) It can access non-static members of the outer class.  
B) It requires an instance of the outer class to be instantiated.  
C) It can only be declared within a static method.  
D) It does not require an outer class instance to be instantiated.

---

# 7. Exceptions
What is true about the 'finally' block in a try-catch-finally structure?

A) It is executed only if an exception is thrown.  
B) It is not executed if an exception is caught in the 'catch' block.  
C) It is executed regardless of whether an exception is thrown or caught.  
D) It will not execute if the 'catch' block contains a return statement.

---

# 8. Annotations
What is the primary use of the `@Deprecated` annotation in Java?

A) To mark a method or class that should not be used anymore.  
B) To indicate that a method or class is going to be removed in future versions.  
C) To automatically document methods or classes.  
D) To prevent a method or class from being serialized.

---

# 9. Reflection
Which statement is true about Reflection in Java?

A) It allows an application to observe and modify its own behavior at runtime.  
B) Reflection can only be used to inspect objects, not modify them.  
C) Using Reflection significantly improves the performance of the application.  
D) Reflection is primarily used for compile-time type checking.

---

# 10. Encapsulation
What encapsulation property is violated if a class has public data fields?

A) Data Hiding  
B) Inheritance  
C) Polymorphism  
D) Abstraction

---

# 11. Inheritance
What happens when a subclass in Java has a method with the same signature as a method in the superclass?

A) The method in the subclass is hidden.  
B) The method in the superclass is overridden.  
C) A compilation error occurs.  
D) The method in the superclass is overloaded.

---

# 12. Abstract Classes
Which statement is true about abstract classes in Java?

A) An abstract class can have both abstract and non-abstract methods.  
B) If a class has at least one abstract method, it must be declared abstract.  
C) An abstract class cannot have a constructor.  
D) Both A and B.

---

# 13. Generic Types
What is the purpose of wildcards (?) in Java generics?

A) To specify an unknown type.  
B) To enforce type safety.  
C) To allow the creation of generic instances.  
D) To restrict a type to a specific class hierarchy.

---

# 14. Collections Framework
In the Java Collections Framework, which is a true statement about the HashSet and TreeSet classes?

A) HashSet maintains elements in sorted order, while TreeSet does not.  
B) TreeSet allows duplicate elements, but HashSet does not.  
C) HashSet offers constant time performance for basic operations, while TreeSet does not.  
D) Both HashSet and TreeSet are synchronized.

---

# 15. Java Annotations and Reflection
What is the primary use of annotations in Java?

A) To change the behavior of a method at runtime.  
B) To provide metadata about the code.  
C) To optimize the code during compilation.  
D) To allocate memory during runtime.

---

# 16. Threads
What is the purpose of the wait() method in Java's object threading?

A) To send the current thread into a waiting state until another thread calls notify().  
B) To permanently stop the execution of the current thread.  
C) To pause the thread for a specific period.  
D) To check if a thread is waiting.

---

# 17. Threads and Synchronization
Which of the following is true about the synchronized keyword in Java?

A) It is used to start a thread.  
B) It can be applied to variables.  
C) It allows only one thread to access a method or block at a time.  
D) It makes the class thread-safe automatically.

---

# 18. Daemon Threads
What is a daemon thread in Java?

A) A high-priority thread.  
B) A thread that does garbage collection.  
C) A thread that runs in the background.  
D) The only thread that can access the main method.

---

# 19. Java I/O
Which of these classes is used to read character files in Java?

A) FileOutputStream  
B) FileReader  
C) BufferedOutputStream  
D) InputStreamReader  

---

# 20. Java I/O
What is the purpose of the BufferedReader class?

A) To write text to a character-output stream.  
B) To read text from a character-input stream, buffering characters for efficient reading.  
C) To handle binary data instead of text data.  
D) To send output to the console.

---
