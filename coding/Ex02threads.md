
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


### Exercise 1 example

1. **Create the `Logger` Class:**

   - The `Logger` class should implement the `Runnable` interface.
   - The class should have a constructor that accepts a `Vector<String>` for storing log messages.

   ```java
   import java.io.FileWriter;
   import java.io.IOException;
   import java.io.PrintWriter;
   import java.util.Vector;

   public class Logger implements Runnable {
       private Vector<String> logMessages;
       private volatile boolean running = true;

       public Logger(Vector<String> logMessages) {
           this.logMessages = logMessages;
       }

       @Override
       public void run() {
           try (PrintWriter writer = new PrintWriter(new FileWriter("activity_log.txt", true))) {
               while (running || !logMessages.isEmpty()) {
                   String message = null;
                   synchronized (logMessages) {
                       if (!logMessages.isEmpty()) {
                           message = logMessages.remove(0);
                       }
                   }
                   if (message != null) {
                       writer.println(message);
                   }
                   Thread.sleep(100); // Small delay to reduce busy-waiting
               }
           } catch (IOException | InterruptedException e) {
               e.printStackTrace();
           }
       }

       public void shutdown() {
           running = false;
       }
   }
   ```

2. **Initialize Logger in Main Application:**

   - In the main application, create a `Vector<String>` to store log messages.
   - Instantiate the `Logger` class and start it in a new thread.
   - Provide a method to log user activities by adding messages to the `Vector`.

   ```java
   import java.util.Vector;

   public class MainApp {
       private static Vector<String> logMessages = new Vector<>();
       private static Logger logger = new Logger(logMessages);
       private static Thread loggerThread = new Thread(logger);

       public static void main(String[] args) {
           loggerThread.start();

           // Simulating user activities
           logActivity("User bob logged in.");
           logActivity("User alice created a new product.");
           logActivity("User bob logged out.");

           // Shutdown the logger thread before exiting
           logger.shutdown();
           try {
               loggerThread.join();
           } catch (InterruptedException e) {
               e.printStackTrace();
           }
       }

       public static void logActivity(String message) {
           synchronized (logMessages) {
               logMessages.add(message);
           }
       }
   }
   ```

3. **Logging User Activities:**

   - In the `logActivity` method, add messages to the `Vector` inside a synchronized block to ensure thread safety.
   - This method can be called throughout the application to log various activities such as user login, logout, and product addition.

4. **Shutdown Logger Gracefully:**

   - The `Logger` class includes a `shutdown` method to set the `running` flag to false.
   - Before the main application exits, call `logger.shutdown()` and then join the logger thread to ensure it finishes processing any remaining log messages.

### Summary

By following these steps, you will:
1. Create a `Logger` class that implements `Runnable` and processes log messages in a separate thread.
2. Use `Vector` for thread-safe storage of log messages.
3. Write log messages to a file in the `run` method.
4. Integrate the logger with the main application to log user activities and shut down the logger gracefully.

These detailed hints should help you implement the user activity logger effectively using `Vector`.
