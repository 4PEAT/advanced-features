## Task: Multi-threaded Library Management System

### Objective:
Create a multi-threaded library management system where multiple threads represent users borrowing and returning books from a shared library. This task will involve using synchronization, wait, notify, interrupt, join, and handling potential deadlocks.

### Requirements:

1. **Book Class**:
   - **Fields**:
     - `bookId`: A unique identifier for the book.
     - `title`: The title of the book.
     - `available`: A boolean indicating if the book is available for borrowing.
   - **Methods**:
     - `synchronized borrow()`: Allows a user to borrow the book if it's available; otherwise, waits until the book becomes available.
     - `synchronized returnBook()`: Allows a user to return the book and notifies any waiting threads.

2. **Library Class**:
   - **Fields**:
     - `books`: A collection (e.g., a `Map` or `List`) of `Book` objects.
   - **Methods**:
     - `synchronized addBook(Book book)`: Adds a book to the library.
     - `synchronized getBook(int bookId)`: Retrieves a book by its ID, or returns null if the book doesn't exist.

3. **User Thread Class**:
   - **Fields**:
     - `userId`: A unique identifier for the user.
     - `library`: A reference to the shared `Library` object.
   - **Methods**:
     - `run()`: The main logic for the thread, which attempts to borrow and return books in a loop.
     - `borrowBook(int bookId)`: Attempts to borrow a book from the library.
     - `returnBook(int bookId)`: Returns a book to the library.

4. **LibraryManagementSystem Class**:
   - **Methods**:
     - `main(String[] args)`: The entry point of the application, which sets up the library and user threads.
     - Initializes the library with a set of books.
     - Starts multiple user threads.
     - Uses `join` to wait for all user threads to finish.

5. **Synchronization and Waiting**:
   - Use synchronization to ensure that book borrowing and returning operations are thread-safe.
   - Use `wait` and `notify` to handle users waiting for books to become available.

6. **Interrupt and Join**:
   - Implement a mechanism to interrupt user threads if they are waiting too long to borrow a book.
   - Use `join` to ensure that the main thread waits for all user threads to finish before terminating.

7. **Deadlock Scenario**:
   - Simulate a potential deadlock scenario by having users attempt to borrow multiple books simultaneously.
   - Implement a mechanism to detect and resolve deadlocks, such as a timeout or deadlock detection algorithm.

---

### Guide to Solve:

#### Step 1: Implement the `Book` Class
- Define the fields `bookId`, `title`, and `available`.
- Implement the `borrow()` method, which should be synchronized and use `wait()` if the book is not available.
- Implement the `returnBook()` method, which should be synchronized and use `notify()` to notify waiting threads.

#### Step 2: Implement the `Library` Class
- Define a collection to hold `Book` objects (e.g., a `Map` or `List`).
- Implement the `addBook()` method to add books to the library.
- Implement the `getBook()` method to retrieve a book by its ID.

#### Step 3: Implement the `User` Class
- Define the fields `userId` and `library`.
- Implement the `run()` method, which should contain a loop where the user attempts to borrow and return books.
- Implement the `borrowBook()` and `returnBook()` methods.

#### Step 4: Implement the `LibraryManagementSystem` Class
- Initialize the library with a set of books.
- Create and start multiple `User` threads.
- Use `join()` to wait for all user threads to finish.
- Implement a mechanism to interrupt user threads after a certain period.

#### Step 5: Handle Synchronization and Waiting
- Ensure that the `borrow()` and `returnBook()` methods in the `Book` class are synchronized.
- Use `wait()` and `notify()` appropriately to manage thread waiting and notification.

#### Step 6: Handle Interrupts and Joins
- Implement logic in the `LibraryManagementSystem` class to interrupt user threads if they take too long.
- Use `join()` to ensure the main thread waits for all user threads to finish.

#### Step 7: Simulate and Handle Deadlocks
- Simulate deadlock by having users attempt to borrow multiple books simultaneously.
- Implement a deadlock detection and resolution mechanism. This could involve setting a timeout for borrowing attempts or using a more sophisticated deadlock detection algorithm.
