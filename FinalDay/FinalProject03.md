### Task: Develop a Console-Based Inventory Management System in Java

**Objective:** Design and implement a console-based Inventory Management System (IMS) in Java that utilizes advanced Object-Oriented Programming (OOP) principles and Java features to manage a collection of products in an inventory. This system should allow users to add, update, view, and delete product information through a simple console interface, without the need for a graphical user interface.

#### System Features and Requirements:

1. **Product Management:**
   - **Inheritance and Abstraction:** Design a base `Product` class with common attributes (e.g., ID, name, price) and methods. Extend this class to create specific product types (e.g., `Electronics`, `Groceries`), demonstrating inheritance.
   - **Composition:** Utilize composition to include features like `PriceTag` (containing price and currency) or `Manufacturer` details within product classes.
   - **Polymorphism and Interfaces:** Implement interfaces for behaviors applicable to subsets of products (e.g., `Refundable`, `Expirable`).

2. **Inventory Operations:**
   - **Enumerations:** Use enumerations to define categories or status codes for products (e.g., `ProductCategory`, `ProductStatus`).
   - **Exceptions:** Implement custom exceptions for handling common inventory errors (e.g., `ProductNotFoundException`, `InventoryFullException`).

3. **Data Handling:**
   - **Generic Types:** Create generic methods or classes for operations that can be applied to any product type, enhancing code reuse.
   - **Collections:** Use Java collections (e.g., `ArrayList`, `HashMap`) to manage the inventory, supporting dynamic data manipulation.
   - **File I/O:** Integrate file I/O to save and load inventory data from files, using `FileReader`, `FileWriter`, and related classes.

4. **System Interaction:**
   - **Console Interface:** Develop a text-based user interface using `System.out` for output and `Scanner` for input, providing a menu-driven system to interact with the inventory.
   - **Commands and Validation:** Implement commands for adding, viewing, updating, and deleting products, including input validation to handle user errors gracefully.

5. **Advanced Java Features:**
   - **Annotations and Reflection:** Use annotations to mark deprecated methods or for documentation purposes. Employ reflection to inspect or modify runtime behavior of classes.
   - **Threads and Concurrency:** Implement basic threading for tasks like background data saving or inventory checks, using synchronization to manage concurrent access to inventory data.

#### Example Console Interface Structure:

```java
import java.util.Scanner;

public class InventoryManagementSystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean exit = false;

        while (!exit) {
            System.out.println("\n--- Inventory Management System ---");
            System.out.println("1. Add Product");
            System.out.println("2. View Product");
            System.out.println("3. Update Product");
            System.out.println("4. Delete Product");
            System.out.println("5. List All Products");
            System.out.println("6. Exit");
            System.out.print("Select an option: ");

            int choice = scanner.nextInt();
            scanner.nextLine(); // Consume newline

            switch (choice) {
                case 1:
                    // Implement Add Product
                    break;
                case 2:
                    // Implement View Product
                    break;
                case 3:
                    // Implement Update Product
                    break;
                case 4:
                    // Implement Delete Product
                    break;
                case 5:
                    // Implement List All Products
                    break;
                case 6:
                    exit = true;
                    System.out.println("Exiting...");
                    break;
                default:
                    System.out.println("Invalid option. Please try again.");
            }
        }
        scanner.close();
    }
}
```

#### Deliverables:

- **Source Code:** Organized and commented Java files for all classes and interfaces.
- **README File:** Compilation and running instructions, alongside usage guidelines for the system.
- **Documentation:** A detailed description of the system architecture, including class diagrams and explanations of how Java features were applied to meet the design goals.

