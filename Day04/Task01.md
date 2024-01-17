**Task: Create and Utilize Custom Java Annotations**

1. **Define a Custom Annotation**: Create a custom annotation named `@Info`. This annotation should be able to store information like `author` and `version`. The annotation should be applicable to classes and methods.

2. **Apply the Annotation**: Use the `@Info` annotation on a class named `MyClass` and on one of its methods. Set different values for `author` and `version` in each case.

3. **Process the Annotation**: Write a method or class (e.g., `AnnotationProcessor`) that can process these annotations. When run, it should read the annotations from `MyClass` and its method, then print out the `author` and `version` values stored in the annotations.

4. **Test the Implementation**: Create a main method in which you create an instance of `MyClass` and call the `AnnotationProcessor` to demonstrate that it correctly identifies and processes the annotations.

This task will help you understand how to define, apply, and process custom annotations in Java, providing a practical understanding of Java's reflection capabilities and annotation processing.
