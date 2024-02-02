
### Project Task: Library Management System

**Overview:**
Design and implement a Library Management System in Java. This system should manage books, patrons (members), and the borrowing process, utilizing various OOP principles and Java features.

**Requirements:**

1. **OOP Principles:**
   - **Inheritance:** Create classes like `Book`, `Member`, `Staff` with common base classes where appropriate.
   - **Composition:** Use composition for relationships (e.g., a `Library` has members and books).
   - **Polymorphism:** Implement polymorphic behavior for different user types (e.g., staff vs. members) or book types.
   - **Encapsulation:** Use private fields and public getters/setters.
   - **Abstraction:** Define abstract classes or interfaces for common operations like `search`, `borrow`, and `return`.

2. **Abstract Classes and Interfaces:**
   - Define interfaces for operations like `Searchable`, `Borrowable`.
   - Use abstract classes for common attributes and methods, such as a `User` class from which `Member` and `Staff` inherit.

3. **Inner and Anonymous Classes:**
   - Use an inner class for functionality like `LibraryHistory`, which tracks borrowing history.
   - Implement anonymous classes for handling events such as a book return or a late fee calculation.

4. **Enumerations:**
   - Define enumerations for categories like `BookGenre`, `MembershipType`.

5. **Exceptions:**
   - Create custom exceptions like `BookNotFoundException`, `MemberLimitExceededException`.

6. **Generic Types:**
   - Use generics for methods like `borrowItems` which can handle different types of borrowable items (e.g., books, magazines).

7. **Collections:**
   - Utilize collections like `List`, `Map` for managing books, members.

8. **Annotations and Reflection:**
   - Use annotations to mark overridden methods, deprecated methods or for serialization purposes.
   - Utilize reflection for features like inspecting class properties or implementing a generic toString method.

**Task:**
Implement the system with the following features:
- Adding/removing books or members.
- Searching for books by title, author, or genre.
- Borrowing and returning books.
- Tracking member borrowing history.
- Handling exceptions for cases like book unavailability.
- Utilizing annotations for logging or tracking method usage.

**Optional Extensions:**
- Implement a simple UI for interaction with the system.
- Add a feature to calculate fines for late returns.
- Use Java Reflection for a feature like dynamic property listing of objects.

**Deliverables:**
- Complete source code of the application.
- Documentation including design choices and UML diagrams.
- Test cases demonstrating the use of various OOP features and Java functionalities.

This task allows for the exploration and application of a wide range of Java OOP concepts in a real-world scenario, ensuring a deep understanding of these principles.
