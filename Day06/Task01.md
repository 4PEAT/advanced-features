### Task: Generic Inventory Management System

#### Objective:
Develop a Java program to manage a generic inventory system. The program should utilize generics to handle various types of items in the inventory.

#### Requirements:

1. **Generic Class `InventoryItem<T>`**:
    - Create a generic class `InventoryItem<T>` where `T` represents the type of the item detail.
    - The class should have a generic attribute `T detail` to store specific information about the item.
    - Include a String attribute `name` for the item's name and an int attribute `quantity` for the quantity in stock.
    - Implement getters and setters for all attributes.

2. **Generic Methods**:
    - Add a generic method `updateDetail(T newDetail)` in the `InventoryItem` class to update the item's detail.
    - Implement a generic method `printItemDetails()` that prints the item's name, quantity, and detail.

3. **Generic Class `InventoryManager<T>`**:
    - Create a generic class `InventoryManager<T>` to manage an array list of `InventoryItem<T>`.
    - Implement methods to add, remove, and display items in the inventory.

4. **Demonstration in Main Class**:
    - Demonstrate the use of `InventoryManager` with at least two different types of item details, such as `String` (e.g., a description) and `Integer` (e.g., a code number).

#### Task Steps:

1. Define the `InventoryItem<T>` class with necessary attributes, methods, and generic types.
2. Implement `updateDetail(T newDetail)` and `printItemDetails()` methods in `InventoryItem<T>`.
3. Create the `InventoryManager<T>` class with methods to manage inventory items.
4. In the main method, create instances of `InventoryManager` for different item types and demonstrate adding, removing, and displaying items.

#### Expected Output:
- The program should be able to handle different types of item details seamlessly.
- When items are added, updated, or removed from the inventory, the changes should be reflected accurately.

#### Example Usage:
- Create an inventory of books with a String detail for the author's name.
- Create an inventory of electronics with an Integer detail for a model number.

This task will help you understand how to use generics in Java to create flexible and reusable code that can handle various data types while maintaining type safety.
