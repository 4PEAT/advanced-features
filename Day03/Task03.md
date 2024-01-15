### Task: Implement an Online Library System in Java

#### Objective
Develop a mini online library system in Java, where users can add books by purchasing them and retrieve existing books from the library.

#### Task Details

**1. Define the `Book` Class**
   - Create a `Book` class with the following parameters:
     - `title` (String)
     - `author` (String)
     - `genre` (String)
     - `price` (double)

**2. Define Custom Exceptions**
   - Create two new exceptions extending `Exception`:
     - `NotEnoughMoneyException`: Thrown when the user does not have enough funds to purchase a book.
     - `NoSuchBookException`: Thrown when the requested book is not found in the library.

**3. Implement the `OnlineLibrary` Class**
   - The class should have:
     - Two parameters: a list of books (`List<Book>`) and the user's budget (`double`).
     - A constructor that accepts the initial budget of the user.
   - Implement methods:
     - `addBook(Book book)`: Adds a book to the library if the user has sufficient funds. Throws `NotEnoughMoneyException` if funds are insufficient.
     - `getBook(String title)`: Returns the requested book if it is in the library. Throws `NoSuchBookException` if the book is not found.

**4. Main Method Implementation**
   - In the `main` method, complete the following tasks:
     - **TODO1**: Add a list of books to the library.
     - **TODO2**: Attempt to retrieve the book titled "book4" from the library. If it doesn't exist, add it.
   - Ensure proper exception handling:
     - Display appropriate messages for each exception case as per the examples given.

#### Guidelines
- Make sure to handle exceptions gracefully, providing clear and informative messages to the user.
- Implement necessary getters, setters, and constructors in your classes.
- Ensure your code is clean, well-commented, and adheres to Java coding standards.

#### Deliverables
- Java source files for `Book`, `NotEnoughMoneyException`, `NoSuchBookException`, and `OnlineLibrary` classes.
- A Java source file with the `main` method to demonstrate the functionality of your library system.
- Documentation or comments within the code explaining your implementation and any assumptions made.

This task aims to assess your ability to work with object-oriented programming concepts in Java, including class design, exception handling, and basic data management.
