
### Java Annotations and Reflection Quiz

**1. What is the primary use of annotations in Java?**
   - A) To change the behavior of a method at runtime
   - B) To provide metadata about the code
   - C) To optimize the code during compilation
   - D) To allocate memory during runtime

**2. Which of these is not a built-in annotation in Java?**
   - A) `@Deprecated`
   - B) `@Override`
   - C) `@FunctionalInterface`
   - D) `@MemoryManagement`


**3. What is Reflection used for in Java?**
   - A) To create new instances of classes at runtime
   - B) To inspect classes, methods, and fields at runtime
   - C) To enhance the performance of the application
   - D) Both A and B


**4. Which method is used to obtain the `Class` object of a class in Java?**
   - A) `getClass()`
   - B) `getType()`
   - C) `instanceOf()`
   - D) `forName()`


**5. Which of these is a correct way to access a private field of a class using Reflection?**
   - A) Using `getField()` method of the `Class` class
   - B) Using `getDeclaredField()` method of the `Class` class and setting it accessible
   - C) Directly accessing the field as Reflection bypasses access control
   - D) Using `getPrivateField()` method of the `Class` class


**6. What does the `@Override` annotation indicate?**
   - A) The annotated method is overriding a method in a superclass.
   - B) The annotated method should be executed over other methods.
   - C) The annotated method will replace a method in a superclass.
   - D) The annotated method cannot be overridden by any subclass.


**7. When using Reflection, how do you invoke a private method of a class?**
   - A) By directly calling the method, as Reflection bypasses method visibility
   - B) By getting the method with `getMethod()` and invoking it
   - C) By getting the method with `getDeclaredMethod()`, setting it accessible, and then invoking it
   - D) Private methods cannot be invoked using Reflection

**8. Which of these is true about the `@FunctionalInterface` annotation?**
   - A) It is used to mark interfaces that have exactly one abstract method.
   - B) It is used to create anonymous classes.
   - C) It indicates that the interface will be automatically implemented by the Java compiler.
   - D) It is used to mark all interfaces that are functional.

**9. How is Reflection commonly used?**
   - A) To increase the efficiency of code execution
   - B) For serialization and deserialization of objects
   - C) In high-performance critical applications
   - D) To create plug-in architectures


**10. What is the potential downside of using Reflection in Java?**
    - A) It makes the code more readable and maintainable
    - B) It can lead to performance overhead
    - C) It is not supported in newer versions of Java
    - D) It automatically optimizes the code
