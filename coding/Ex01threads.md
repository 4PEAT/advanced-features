
### Exercise 1: User Activity Logger

**Objective:**
Implement a user activity logger that logs all user activities (e.g., login, logout, post creation) to a file in a separate thread.

**Task:**
1. Create a `Logger` class that implements `Runnable`.
2. In the `run` method, write code to log messages to a file.
3. Use a thread-safe collection (like `Vector` or synchronized list) to pass log messages from the main application to the logger thread.
4. Modify the main application to log user activities such as login, logout, and post creation.

### Exercise 2: Post Fetching Simulation

**Objective:**
Simulate fetching posts in a separate thread to avoid blocking the main thread.

**Task:**
1. Create a `PostFetcher` class that implements `Runnable`.
2. In the `run` method, simulate fetching posts by using `Thread.sleep` and populate a list.
3. Modify the main application to start the `PostFetcher` thread when listing posts by a user.

### Exercise 3: Notification System

**Objective:**
Implement a notification system that sends notifications to users in a separate thread.

**Task:**
1. Create a `Notifier` class that implements `Runnable`.
2. In the `run` method, simulate sending notifications (e.g., new follower, post liked) by printing to the console or writing to a file.
3. Use a thread-safe collection to manage notifications.
4. Modify the main application to send notifications for relevant user activities.

### Exercise 4: Concurrent User Registration

**Objective:**
Allow multiple users to register concurrently without causing data inconsistencies.

**Task:**
1. Implement user registration in a thread-safe manner using synchronization.
2. Create multiple threads to simulate concurrent user registrations.
3. Ensure that the user list remains consistent and no duplicate usernames are allowed.

### Exercise 5: Background Post Cleanup

**Objective:**
Periodically clean up old posts in the background without affecting the main application performance.

**Task:**
1. Create a `PostCleanup` class that implements `Runnable`.
2. In the `run` method, periodically check and delete posts older than a certain threshold using `Thread.sleep` for intervals.
3. Start the `PostCleanup` thread when the application starts and let it run in the background.

### Exercise 6: Thread Pool for User Actions

**Objective:**
Use a thread pool to handle multiple user actions concurrently to improve performance.

**Task:**
1. Create a thread pool using `ExecutorService`.
2. Submit various user actions (e.g., posting, following, liking) as tasks to the thread pool.
3. Ensure that the application can handle multiple user actions simultaneously without performance degradation.

### Exercise 7: Real-time Feed Update

**Objective:**
Implement a system to update the user's feed in real-time using threads.

**Task:**
1. Create a `FeedUpdater` class that implements `Runnable`.
2. In the `run` method, periodically fetch new posts and update the user's feed using `Thread.sleep` for intervals.
3. Start the `FeedUpdater` thread when the user logs in and stop it when the user logs out.

### Exercise 8: Synchronized Follower Count

**Objective:**
Ensure the follower count is updated accurately when multiple users follow/unfollow simultaneously.

**Task:**
1. Implement synchronized methods to increment and decrement the follower count.
2. Simulate multiple threads performing follow/unfollow actions concurrently.
3. Verify that the follower count is consistent and correct after all operations.


### Exercise 1 example

1. **Create the `Logger` Class:**

```java
import java.io.FileWriter;
import java.io.IOException;
import java.io.PrintWriter;
import java.util.concurrent.ConcurrentLinkedQueue;

public class Logger implements Runnable {
    private ConcurrentLinkedQueue<String> logMessages;
    private volatile boolean running = true;

    public Logger(ConcurrentLinkedQueue<String> logMessages) {
        this.logMessages = logMessages;
    }

    @Override
    public void run() {
        try (PrintWriter writer = new PrintWriter(new FileWriter("activity_log.txt", true))) {
            while (running || !logMessages.isEmpty()) {
                String message = logMessages.poll();
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

```java
import java.util.concurrent.ConcurrentLinkedQueue;

public class MainApp {
    private static ConcurrentLinkedQueue<String> logMessages = new ConcurrentLinkedQueue<>();
    private static Logger logger = new Logger(logMessages);
    private static Thread loggerThread = new Thread(logger);

    public static void main(String[] args) {
        loggerThread.start();

        // Simulating user activities
        logActivity("User bob logged in.");
        logActivity("User alice created a new post.");
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
        logMessages.add(message);
    }
}
```

3. **Logging User Activities:**
- In the `logActivity` method, add messages to the `ConcurrentLinkedQueue`.
- This method can be called throughout the application to log various activities such as user login, logout, and post creation.

4. **Shutdown Logger Gracefully:**
- The `Logger` class includes a `shutdown` method to set the `running` flag to false.
- Before the main application exits, call `logger.shutdown()` and then join the logger thread to ensure it finishes processing any remaining log messages.

### Summary

By following these steps, you will:
1. Create a `Logger` class that implements `Runnable` and processes log messages in a separate thread.
2. Use `ConcurrentLinkedQueue` for thread-safe storage of log messages.
3. Write log messages to a file in the `run` method.
4. Integrate the logger with the main application to log user activities and shut down the logger gracefully.
