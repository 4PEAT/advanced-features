### Java Programming Assignment: Multi-threaded Restaurant Simulation

**Objective:**
Develop a multi-threaded Java application that simulates the operation of a restaurant with cooks and servers, showcasing your understanding of threading concepts, synchronization, and concurrent programming.

**Background:**
In a restaurant, cooks prepare meals, and servers deliver them to customers. This process involves multiple tasks happening simultaneously, making it a good scenario for a multi-threaded application.

**Assignment Details:**

1. **Classes to Implement:**
   - `Cook`: Represents a cook in the restaurant.
     - Each cook can prepare one dish at a time.
     - Preparing a dish takes a random amount of time (simulate this with `Thread.sleep`).
   - `Server`: Represents a server in the restaurant.
     - Each server can serve one dish at a time to a customer.
     - Serving a dish takes a random amount of time (simulate this with `Thread.sleep`).
   - `Order`: Represents an order placed by a customer.
     - Contains details like order ID and the dish name.
   - `Restaurant`: Main class to coordinate cooks and servers.

2. **Functionality:**
   - The restaurant receives a list of orders (simulate this with a shared data structure, e.g., a `BlockingQueue`).
   - Cooks pick up orders from the list, prepare the dishes, and place them in a completed orders area (another shared data structure).
   - Servers pick up completed dishes and "serve" them (simply print out a message indicating the dish has been served).
   - Ensure proper synchronization between cooks and servers to avoid data inconsistencies.

3. **Requirements:**
   - Use threads to represent the cooks and servers. The number of each should be configurable.
   - Properly handle thread interruption and ensure the application can be stopped gracefully.
   - Use synchronization mechanisms (like `synchronized`, locks, semaphores) to manage access to shared resources (like order lists).
   - Include comments explaining your code and the threading concepts utilized.
   - Ensure that your code is free from common concurrency issues like deadlocks or race conditions.

This assignment will help you understand the practical aspects of multi-threaded programming in Java, focusing on coordination between threads, resource sharing, and synchronization challenges. Good luck!
