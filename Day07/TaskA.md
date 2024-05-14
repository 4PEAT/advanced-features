### Task: Implement a Java Program to Simulate a Multi-threaded Countdown Timer

#### Objectives:
1. Create a custom thread class to perform a countdown.
2. Use `interrupt()` to stop threads prematurely.
3. Use `join()` to wait for thread completion.
4. Override the `run()` method to define the thread's behavior.

#### Instructions:
1. **Create a Custom Thread Class**:
    - Create a class named `CountdownThread` that extends `Thread`.
    - This class should have a constructor that accepts an integer `startNumber`.
    - Override the `run()` method to count down from `startNumber` to 0.
    - Inside the `run()` method, use a loop to print the current number being counted down.

2. **Handle Interruptions**:
    - Inside the loop, check if the thread has been interrupted using `Thread.interrupted()`.
    - If the thread is interrupted, print a message indicating the interruption and terminate the loop.
    - Simulate work inside the loop using `Thread.sleep(1000)`.
    - Handle `InterruptedException` by printing a message and setting the interrupt flag again using `Thread.currentThread().interrupt()`.

3. **Create and Start Threads**:
    - In the `main` method of your program, create three instances of `CountdownThread` with different `startNumber` values.
    - Start all three threads.

4. **Interrupt Threads**:
    - After starting the threads, let the main thread sleep for a few seconds using `Thread.sleep(5000)`.
    - Interrupt all `CountdownThread` instances using the `interrupt()` method.

5. **Wait for Thread Completion**:
    - Use the `join()` method to wait for all threads to finish.

6. **Print Completion Message**:
    - After all threads have completed, print a message from the main thread indicating that all threads have finished.

### Example Output
```
Thread-0 counts down: 10
Thread-1 counts down: 15
Thread-2 counts down: 20
Thread-0 counts down: 9
Thread-1 counts down: 14
Thread-2 counts down: 19
...
Thread-0 was interrupted.
Thread-1 was interrupted.
Thread-2 was interrupted.
Main thread has finished.
```

### Hints
- Use `Thread.sleep(1000)` to simulate one second of countdown.
- Ensure to handle `InterruptedException` properly to manage thread interruptions.
- Remember to call `Thread.currentThread().interrupt()` inside the catch block for `InterruptedException`.

Good luck!
