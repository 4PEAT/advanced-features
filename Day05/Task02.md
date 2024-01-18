### Task: Implement a Document Printing System using a Queue in Java

#### Scenario
You are tasked with creating a basic document printing system for a small office. The office has a single printer, and multiple users send print jobs to this printer. To manage these print jobs efficiently and ensure they are printed in the order they were received, you decide to use a queue.

#### Task Description
1. **Create a Print Job Class**: Define a class `PrintJob` with at least two attributes: a unique `jobId` (e.g., an integer or a string) and a `documentName` (string). Feel free to add more attributes relevant to a print job.

2. **Implement the Print Queue**:
   - Use any appropriate `Queue` implementation from Java Collections Framework to create a print queue.
   - Ensure the queue holds `PrintJob` objects.

3. **Simulate Adding Jobs to the Queue**:
   - Create a method to add print jobs to the queue. Each job should have a unique ID and a document name.
   - Simulate adding multiple print jobs to the queue.

4. **Process the Print Queue**:
   - Implement a method to process the print jobs in the queue.
   - When processing a job, simply print out details of the job being printed and then remove it from the queue.
   - If the queue is empty, display a message indicating that all print jobs have been completed.

5. **Handle Exceptions and Edge Cases**:
   - Ensure your program gracefully handles scenarios such as trying to process a job when the queue is empty.

#### Additional Challenges (Optional)
- Implement functionality to prioritize certain print jobs over others.
- Add a feature to track and display the number of print jobs completed in a day.
- Extend the system to support multiple printers, each with its own print queue.

This task involves concepts such as object-oriented programming, queues, and basic system simulation. It provides a practical scenario to apply Java's queue data structures in a real-world application.
