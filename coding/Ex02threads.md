
### Exercise 1: User Activity Logger

**Objective:**
Implement a user activity logger that logs all user activities (e.g., login, logout, product addition) to a file in a separate thread.

**Task Requirements:**
1. Create a `Logger` class that implements `Runnable`.
2. Use a thread-safe collection to store log messages.
3. Write log messages to a file in the `run` method.
4. Integrate the logger with the main application to log user activities.

**Hint:**
- Use `Vector` for storing log messages.
- Use `synchronized` to ensure thread safety when accessing the log collection.

### Exercise 2: Product Fetching Simulation

**Objective:**
Simulate fetching products in a separate thread to avoid blocking the main thread.

**Task Requirements:**
1. Create a `ProductFetcher` class that implements `Runnable`.
2. Simulate fetching products with `Thread.sleep`.
3. Populate a list with product data in the `run` method.
4. Integrate the `ProductFetcher` thread with the main application to fetch and display products.

**Hint:**
- Use `Thread.sleep` to simulate delay.
- Use `synchronized` blocks to ensure thread safety when accessing the product list.

### Exercise 3: Notification System

**Objective:**
Implement a notification system that sends notifications to users in a separate thread.

**Task Requirements:**
1. Create a `Notifier` class that implements `Runnable`.
2. Use a thread-safe collection to manage notifications.
3. Print notifications to the console or write to a file in the `run` method.
4. Integrate the notifier with the main application to send notifications for user activities.

**Hint:**
- Use `Vector` for storing notifications.
- Use `synchronized` to ensure thread safety when accessing the notification collection.

### Exercise 4: Concurrent User Registration

**Objective:**
Allow multiple users to register concurrently without causing data inconsistencies.

**Task Requirements:**
1. Implement user registration in a thread-safe manner using synchronization.
2. Create multiple threads to simulate concurrent user registrations.
3. Ensure that the user list remains consistent and no duplicate usernames are allowed.

**Hint:**
- Use `synchronized` blocks to manage access to the user collection.
- Ensure that usernames are checked and added in a thread-safe manner.

### Exercise 5: Background Product Cleanup

**Objective:**
Periodically clean up old products in the background without affecting the main application performance.

**Task Requirements:**
1. Create a `ProductCleanup` class that implements `Runnable`.
2. Periodically check and delete products older than a certain threshold using `Thread.sleep` for intervals.
3. Start the `ProductCleanup` thread when the application starts and let it run in the background.

**Hint:**
- Use `Thread.sleep` to control the interval between cleanups.
- Use `synchronized` blocks to ensure thread safety when accessing the product list.
