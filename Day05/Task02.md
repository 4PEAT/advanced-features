Sure, here's a practical task scenario for using a queue in Java, including a task description and the necessary code to implement it.

### Scenario
Imagine you're developing a system for a customer support center. This center receives support tickets which are added to a queue. Each ticket is processed in the order it was received. Your task is to create a system that manages this queue of tickets.

### Task
You need to write a Java program that:

1. **Creates a Queue**: This queue will hold the support tickets. Each ticket can just be a simple string representing a customer query.

2. **Adds Tickets to the Queue**: Simulate ticket arrival by adding several tickets to the queue.

3. **Processes the Tickets**: Remove tickets from the queue one by one, simulating the processing of each ticket. As each ticket is processed, print it out.

4. **Handles an Empty Queue**: The program should gracefully handle the case when the queue is empty.

### Example Java Code

```java
import java.util.LinkedList;
import java.util.Queue;

public class SupportTicketSystem {
    public static void main(String[] args) {
        Queue<String> ticketQueue = new LinkedList<>();

        // Adding tickets to the queue
        ticketQueue.add("Ticket 1: Login Issue");
        ticketQueue.add("Ticket 2: Payment failed");
        ticketQueue.add("Ticket 3: Account locked");

        // Processing the tickets
        while (!ticketQueue.isEmpty()) {
            String currentTicket = ticketQueue.poll(); // Retrieves and removes the head of the queue
            System.out.println("Processing: " + currentTicket);
            // Code to process the ticket can be added here
        }

        // Check if all tickets are processed
        if (ticketQueue.isEmpty()) {
            System.out.println("All tickets have been processed.");
        }
    }
}
```

This program demonstrates a simple use of a queue in a real-world scenario. You can expand this basic framework with additional features like prioritizing certain tickets, handling concurrency in a multi-threaded environment, or integrating it with a database or a front-end interface.
