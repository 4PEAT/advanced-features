
### Java Threading Quiz

**1. What is the purpose of the `wait()` method in Java's object threading?**
   - A) To send the current thread into a waiting state until another thread calls `notify()`
   - B) To permanently stop the execution of the current thread
   - C) To pause the thread for a specific period
   - D) To check if a thread is waiting

**2. Which of the following is true about the `synchronized` keyword in Java?**
   - A) It is used to start a thread
   - B) It can be applied to variables
   - C) It allows only one thread to access a method or block at a time
   - D) It makes the class thread-safe automatically
   - 
**3. What is the main difference between the `Thread` class and the `Runnable` interface in Java?**
   - A) `Thread` is a class, `Runnable` is an interface
   - B) `Runnable` can start a thread, `Thread` cannot
   - C) `Thread` has a `run()` method, `Runnable` does not
   - D) `Runnable` has a `start()` method, `Thread` does not

**4. What is a daemon thread in Java?**
   - A) A high-priority thread
   - B) A thread that does garbage collection
   - C) A thread that runs in the background
   - D) The only thread that can access the main method

**5. Which method would change the name of a thread?**
   - A) `setName()`
   - B) `changeName()`
   - C) `renameThread()`
   - D) `updateName()`

**6. What happens when the `join()` method is called on a thread?**
   - A) The current thread pauses its execution until the thread it joins completes
   - B) The thread immediately stops executing
   - C) The runtime joins two threads into one
   - D) The thread execution is permanently joined to the main thread

**7. How do you ensure that a resource is accessed by only one thread at a time?**
   - A) By using the `volatile` keyword
   - B) By using the `synchronized` keyword
   - C) By using the `static` keyword
   - D) By using the `final` keyword
   - 
**8. In Java, which of these is a correct way to create a new thread?**
   - A) `new Thread(new Runnable()).start();`
   - B) `new Runnable().start();`
   - C) `Thread.start(new Runnable());`
   - D) `Runnable.start(new Thread());`

**9. What is the use of the `interrupt()` method in thread handling in Java?**
   - A) To permanently stop a thread
   - B) To request a thread to stop its current work and do something else
   - C) To combine two threads
   - D) To pause a thread temporarily

**10. Which method checks if a thread has been interrupted?**
    - A) `isInterrupted()`
    - B) `checkInterrupt()`
    - C) `hasInterrupted()`
    - D) `getInterruptStatus()`

