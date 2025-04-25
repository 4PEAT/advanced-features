

# 📋 Task: Develop a Java Program for a Unique Item Tracker

## 🎯 Objective
Create a **Java application** that manages a collection of unique items, each identified by a **unique ID** and associated with a **name**.  
The system must allow users to:
- **Add** items
- **Remove** items
- **Search** for items
- **Display** all items

Duplicate entries (based on the unique ID) must be **prevented**.

---

## 🛠 Requirements

### Setup
- Java Development Kit (JDK)
- Any IDE (e.g., IntelliJ, Eclipse) or a simple text editor.

---

### 1. `Item` Class
- Define a class `Item` with:
  - `id` (String) — Unique identifier.
  - `name` (String) — Item's name.
- Implement:
  - Constructor, getters, and setters.
  - `equals()` and `hashCode()` based **only on `id`** to ensure items with the same ID are considered duplicates.
  - `toString()` for clean item display.

---

### 2. `ItemTracker` Class
- Define a class `ItemTracker` that manages a collection of `Item` objects using a `Set<Item>` (preferably a `HashSet`).
- Implement the following methods:
  - `boolean addItem(Item item)`  
    ➔ Adds an item if the ID is unique.
  - `boolean removeItem(String id)`  
    ➔ Removes an item by ID using `removeIf`.
  - `boolean removeItemIterator(String id)`  
    ➔ Alternative method: removes by iterating manually using an `Iterator`.
  - `Set<Item> searchItemByName(String name)`  
    ➔ Searches items case-insensitively by name using streams.
  - `Set<Item> searchItemByNameWithFor(String name)`  
    ➔ Alternative search method using a classic `for-each` loop.
  - `void displayAllItems()`  
    ➔ Prints all current items.

---

### 3. `Main` Class
- Create a `Main` class to simulate the functionality.
- Steps:
  - Add several items manually.
  - Try adding a duplicate item and display the result.
  - Search for items by name and display results.
  - Remove an item by ID and display confirmation.
  - Display all remaining items.

---

## 📈 Advanced (Optional Enhancements)
- Implement console interaction (scanner input) with a simple menu: add, remove, search, display, exit.
- Support multiple attributes (e.g., price, category) in the `Item` class.
- Implement error handling (e.g., invalid input, non-existing ID).

---

## ✅ Evaluation Criteria
- Correct usage of `Set` to enforce uniqueness.
- Proper implementation of `equals()` and `hashCode()`.
- Clear separation of responsibilities across classes.
- Code readability and structure (clean, consistent, well-named methods).
- Proper handling of duplicate additions and safe removal of items.

---

## 📦 Example Project Structure

```text
collection/
 └── set/
      ├── task01/
      │    ├── Item.java
      │    ├── ItemTracker.java
      │    └── Main.java
```

---

# 💬 Example Flow of Execution

```
Item added: Book
Item added: Laptop
Item added: Phone
Duplicate item ID detected: TV (ID = 2)

All Items:
Item{id='1', name='Book'}
Item{id='2', name='Laptop'}
Item{id='3', name='Phone'}

Searching for 'Laptop':
Item{id='2', name='Laptop'}

Removing item with ID '1': Successful

All Items after removal:
Item{id='2', name='Laptop'}
Item{id='3', name='Phone'}
```

---

# 🧠 Important Concepts Practiced
- Java Collections (`Set`, `HashSet`)
- Overriding `equals()` and `hashCode()`
- Iteration with `Iterator` and Stream API
- Object-Oriented Design (Classes, Encapsulation)
- Basic console interaction and testing

---
