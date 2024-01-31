
**Task** Restaurant Order Management System

**Task Description:**

Imagine you are tasked with developing a multi-threaded Java program for a restaurant's order management system. The system should efficiently handle incoming orders, process them, and notify kitchen staff when orders are ready to be prepared and served.

**Requirements:**

1. Create a Java program for managing orders in a restaurant. The system should include the following components:

   - **Order Queue:** A shared data structure (e.g., a queue or list) for storing incoming customer orders. Orders can be placed by customers and should include details such as the order number, table number, and items ordered.

   - **Chef Threads:** Multiple chef threads responsible for preparing and cooking orders. Each chef thread should take an order from the order queue, cook the items, and mark the order as ready when done.

   - **Waiter Threads:** Multiple waiter threads responsible for serving orders to customers. Waiter threads should take orders marked as ready and serve them to the respective tables.

2. Implement a mechanism for customer threads to place orders into the order queue. Each order should include the table number and a list of items ordered.

3. Implement a way for chef threads to wait when there are no orders in the queue. Chefs should be able to resume cooking when new orders are placed.

4. Implement a way for waiter threads to wait when there are no orders ready to be served. Waiters should be able to resume serving when orders become available.

5. Use `notify` and `notifyAll` appropriately to coordinate the activities of chefs, waiters, and customers.

6. Display status updates in the console or a user interface to show when orders are placed, when they are being prepared, and when they are served.

**Constraints:**

- The system should be able to handle multiple orders from different tables concurrently.
- Implement proper error handling and termination for threads.
- Use suitable data structures for managing orders and synchronization mechanisms to prevent race conditions and deadlocks.
- Ensure that the program terminates gracefully when all orders have been processed and served.

**Evaluation Criteria:**

- Correctness and synchronization of the restaurant order management system.
- Proper use of `wait`, `notify`, and `notifyAll` for thread synchronization.
- Handling of edge cases, errors, and thread termination.
- Clarity and usability of the status updates or user interface.
- Code readability, organization, and comments.

**Additional Notes:**

- You can extend this task by adding features like order priorities, order cancellation, or chef/waiter assignments to specific tables.
- Implementing this task simulates a real-world scenario where multiple entities (customers, chefs, and waiters) interact and coordinate through a shared resource (the order queue). It demonstrates the practical use of thread synchronization techniques.
