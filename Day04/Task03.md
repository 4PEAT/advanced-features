
#### Exercise: Designing an E-commerce System

#### Objective:
The objective of this exercise is to apply OOP principles (encapsulation, inheritance, polymorphism, and abstraction) to design and implement a simple e-commerce system in Java.

#### Description:
You are tasked with creating an e-commerce system that allows you to manage products, customers, and orders. The system should support the following functionalities:

1. Add new products to the catalog.
2. Register new customers.
3. Create and manage customer orders.
4. Display details of products, customers, and orders.

#### Classes to Implement:

1. **Product**:
   - **Attributes**:
     - `String productId`: Unique identifier for each product.
     - `String name`: Name of the product.
     - `double price`: Price of the product.
     - `int stockQuantity`: Quantity of the product available in stock.
   - **Methods**:
     - Constructor to initialize product details.
     - Getters and setters for product attributes.
     - `String toString()`: Method to return a string representation of the product.

2. **Customer**:
   - **Attributes**:
     - `String customerId`: Unique identifier for each customer.
     - `String name`: Name of the customer.
     - `String email`: Email address of the customer.
     - `List<Order> orders`: List of orders placed by the customer.
   - **Methods**:
     - Constructor to initialize customer details.
     - Getters and setters for customer attributes.
     - `void addOrder(Order order)`: Method to add an order to the customer's order list.
     - `String toString()`: Method to return a string representation of the customer.

3. **Order**:
   - **Attributes**:
     - `String orderId`: Unique identifier for each order.
     - `Customer customer`: The customer who placed the order.
     - `List<Product> products`: List of products included in the order.
     - `double totalPrice`: Total price of the order.
   - **Methods**:
     - Constructor to initialize order details.
     - Getters and setters for order attributes.
     - `void addProduct(Product product)`: Method to add a product to the order.
     - `void calculateTotalPrice()`: Method to calculate the total price of the order.
     - `String toString()`: Method to return a string representation of the order.

4. **ECommerceSystem**:
   - **Attributes**:
     - `List<Product> productCatalog`: List of all products available in the e-commerce system.
     - `List<Customer> customers`: List of all registered customers.
     - `List<Order> orders`: List of all orders placed in the system.
   - **Methods**:
     - Constructor to initialize the system.
     - `void addProduct(Product product)`: Method to add a product to the product catalog.
     - `void registerCustomer(Customer customer)`: Method to register a new customer.
     - `Order createOrder(String customerId, List<String> productIds)`: Method to create a new order for a customer.
     - `void displayAllProducts()`: Method to display details of all products.
     - `void displayAllCustomers()`: Method to display details of all customers.
     - `void displayAllOrders()`: Method to display details of all orders.

#### Task:

1. **Define the Product Class**:
   - Create the `Product` class with the specified attributes (`productId`, `name`, `price`, `stockQuantity`).
   - Implement a constructor to initialize the product details.
   - Provide getters and setters for the product attributes.
   - Implement the `toString` method to return a string representation of the product.

2. **Define the Customer Class**:
   - Create the `Customer` class with the specified attributes (`customerId`, `name`, `email`, `orders`).
   - Implement a constructor to initialize the customer details.
   - Provide getters and setters for the customer attributes.
   - Implement the `addOrder` method to add an order to the customer's order list.
   - Implement the `toString` method to return a string representation of the customer.

3. **Define the Order Class**:
   - Create the `Order` class with the specified attributes (`orderId`, `customer`, `products`, `totalPrice`).
   - Implement a constructor to initialize the order details.
   - Provide getters and setters for the order attributes.
   - Implement the `addProduct` method to add a product to the order.
   - Implement the `calculateTotalPrice` method to calculate the total price of the order.
   - Implement the `toString` method to return a string representation of the order.

4. **Define the ECommerceSystem Class**:
   - Create the `ECommerceSystem` class with the specified attributes (`productCatalog`, `customers`, `orders`).
   - Implement a constructor to initialize the system.
   - Implement the `addProduct` method to add a product to the product catalog.
   - Implement the `registerCustomer` method to register a new customer.
   - Implement the `createOrder` method to create a new order for a customer. This method should:
     - Find the customer by `customerId`.
     - Find the products by `productIds`.
     - Create a new `Order` object.
     - Add the order to the customer's order list and the system's order list.
     - Calculate the total price of the order.
   - Implement the `displayAllProducts` method to display details of all products.
   - Implement the `displayAllCustomers` method to display details of all customers.
   - Implement the `displayAllOrders` method to display details of all orders.

5. **Main Class**:
   - Write a `Main` class to test the functionality of the e-commerce system.
   - Create instances of products, customers, and orders.
   - Add products to the product catalog.
   - Register customers.
   - Create orders for customers.
   - Display details of products, customers, and orders to ensure the system works as expected.
