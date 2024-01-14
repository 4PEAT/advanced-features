### Task: Implement an Enum for Traffic Light Signals

#### Objective:
Develop a Java program that uses an enum to represent traffic light signals (Red, Yellow, Green) and simulates a simple traffic light control system.

#### Requirements:

1. **Enum Creation**:
   - Create an enum named `TrafficSignal` with three constants: RED, YELLOW, GREEN.
   - Each constant should have two attributes: `duration` (int, representing seconds the signal lasts) and `message` (String, representing a message to be displayed).

2. **Enum Constructor and Methods**:
   - Define a private constructor in `TrafficSignal` that accepts `duration` and `message` as parameters.
   - Implement two public getter methods in the enum to access these attributes.

3. **Main Method Implementation**:
   - In your `main` method, write a loop to iterate over each `TrafficSignal` constant.
   - For each signal, print out the signal's name, its duration, and its message.
   - Simulate the traffic light sequence by making the program wait for the duration of each signal before moving to the next (Hint: use `Thread.sleep` for the delay).

4. **Signal Change Logic**:
   - After completing one cycle (Red -> Yellow -> Green), the program should start the cycle again.
   - The program should complete three full cycles of traffic light changes.

5. **Exception Handling**:
   - Handle any potential `InterruptedException` that might be thrown due to the use of `Thread.sleep`.

#### Example Output:
```
RED Signal: Stop for 30 seconds.
(wait for 30 seconds)
YELLOW Signal: Get ready for 5 seconds.
(wait for 5 seconds)
GREEN Signal: Go for 60 seconds.
(wait for 60 seconds)
... (Repeat for two more cycles)
```

#### Additional Challenge (Optional):
For an additional challenge, modify your program to randomly assign durations to signals within a specified range each time a new cycle starts, making the traffic light changes less predictable.
