

# 📋 Task: Implement a Document Printing System Using a Queue in Java

## 🎯 Objective
Develop a **simple document printing system** that manages and processes print jobs in the **order they are received** (FIFO — First-In, First-Out), using a **Queue** from Java Collections Framework.

---

## 🛠 Task Details

### 1. Create the `PrintJob` Class
- Define a class called `PrintJob` with the following attributes:
  - `jobId` (int) — a **unique** auto-incremented ID for each print job.
  - `documentName` (String) — the name of the document to be printed.
- Implement:
  - A constructor that automatically assigns a new unique `jobId` when a new `PrintJob` is created.
  - `getters` for both fields.
  - `toString()` method to display job details nicely.

---

### 2. Create the `PrintQueue` Class
- Define a class called `PrintQueue` that internally uses a `Queue<PrintJob>` (for example, a `LinkedList`).
- Implement the following methods:
  - `void addJob(PrintJob job)` — Adds a new print job to the queue.
  - `void processJobs()` — Processes (prints) all jobs in the queue, one by one:
    - For each job, print its details to the console.
    - After all jobs are processed, display a final message ("All print jobs have been completed.").
  - Handle the case where there are no jobs to process gracefully (without throwing errors).

---

### 3. Create the `Main` Class
- Simulate the system:
  - Create an instance of `PrintQueue`.
  - Add several `PrintJob` objects to the queue.
  - Process all print jobs by calling `processJobs()`.

---

## 📈 Optional (Advanced Enhancements)
- Add a short delay (`Thread.sleep`) between printing each job to simulate real-world printing.
- Implement a priority system where certain jobs (like "urgent" documents) are processed before others.
- Track the number of jobs printed during the session.
- Support multiple printers (each printer having its own queue).

---

## ✅ Requirements
- Use a **Queue** to maintain the order of print jobs.
- Ensure that **each job** has a **unique ID** and a **document name**.
- Ensure **all jobs are processed in the order they were added** (FIFO behavior).
- Code must be clean, readable, and follow good object-oriented principles.

---

# 📦 Example Project Structure

```text
collection/
 └── set/
      └── task02/
          ├── Main.java
          ├── PrintJob.java
          └── PrintQueue.java
```

---

# 💬 Expected Output Example

```
Printing: PrintJob{jobId=1, documentName='Document1.pdf'}
Printing: PrintJob{jobId=2, documentName='Document2.pdf'}
Printing: PrintJob{jobId=3, documentName='Document3.pdf'}
All print jobs have been completed.
```

---

# 🧠 Concepts Practiced
- Java Collections Framework (`Queue`)
- Object-Oriented Programming (Classes, Objects, Encapsulation)
- FIFO (First-In, First-Out) behavior simulation
- Basic system simulation (real-world analogy)
