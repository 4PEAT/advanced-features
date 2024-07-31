
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

### Example Code Snippets

Here are some example code snippets to get you started with these exercises:

#### Logger Example
```java
import java.io.FileWriter;
import java.io.IOException;
import java.io.PrintWriter;
import java.util.ArrayList;
import java.util.List;

class Logger implements Runnable {
    private List<String> logMessages;

    public Logger(List<String> logMessages) {
        this.logMessages = logMessages;
    }

    @Override
    public void run() {
        try (PrintWriter writer = new PrintWriter(new FileWriter("log.txt", true))) {
            while (true) {
                synchronized (logMessages) {
                    if (!logMessages.isEmpty()) {
                        writer.println(logMessages.remove(0));
                    }
                }
                Thread.sleep(100); // Small delay to reduce busy-waiting
            }
        } catch (IOException | InterruptedException e) {
            e.printStackTrace();
        }
    }
}

// In the main application
List<String> logMessages = new ArrayList<>();
Logger logger = new Logger(logMessages);
Thread loggerThread = new Thread(logger);
loggerThread.start();

// Example of logging a user login
synchronized (logMessages) {
    logMessages.add("User bob logged in.");
}
```

#### Post Fetcher Example
```java
import java.util.List;

class PostFetcher implements Runnable {
    private String username;
    private List<String> posts;

    public PostFetcher(String username, List<String> posts) {
        this.username = username;
        this.posts = posts;
    }

    @Override
    public void run() {
        try {
            Thread.sleep(2000); // Simulate delay
            synchronized (posts) {
                posts.add("Post 1 by " + username);
                posts.add("Post 2 by " + username);
            }
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }
    }
}

// In the main application
List<String> posts = new ArrayList<>();
PostFetcher postFetcher = new PostFetcher("bob", posts);
Thread postFetcherThread = new Thread(postFetcher);
postFetcherThread.start();
postFetcherThread.join(); // Wait for the fetcher to finish

// Display fetched posts
synchronized (posts) {
    for (String post : posts) {
        System.out.println(post);
    }
}
```
