#### 6. User Profile Management

**User Profile:**
- **Attributes:**
  - User's email address.
  - Delivery address.
  - Order history.

**User Profile Management:**
- **Update Profile:**
  - Allow users to update their email and delivery address.
  - Provide feedback indicating whether the update was successful or if there was an error.
- **View Order History:**
  - Allow users to view their past purchases.
  - Display order details such as product name, quantity, purchase date, and total cost.

#### 7. Product Search and Filtering

**Search Functionality:**
- **Search Products:**
  - Allow users to search for products by name or part of the name.
  - Display search results with product details.
- **Filter Products:**
  - Allow users to filter products based on criteria such as price range and stock availability.
  - Display filtered results with product details.

#### 8. Shopping Cart

**Shopping Cart Management:**
- **Add to Cart:**
  - Allow users to add products to their shopping cart.
  - Provide feedback indicating whether the addition was successful or if there was an error.
- **View Cart:**
  - Allow users to view the contents of their shopping cart.
  - Display product details, quantity, and total cost.
- **Remove from Cart:**
  - Allow users to remove products from their cart.
  - Provide feedback indicating whether the removal was successful or if there was an error.
- **Checkout:**
  - Allow users to purchase all items in their cart.
  - Validate stock availability and update the stock.
  - Clear the cart after successful purchase.
  - Provide feedback indicating whether the purchase was successful or if there was an error.

#### 9. Order Management

**Order Handling:**
- **Generate Order ID:**
  - Generate a unique order ID for each purchase.
- **Record Order:**
  - Store order details such as order ID, products, quantity, total cost, and purchase date.
- **Order Confirmation:**
  - Provide users with an order confirmation message including order ID and summary.

### Expanded Console Menu Example

```plaintext
Welcome to the Enhanced E-Commerce Platform!

Main Menu:
1. Register a new user
2. Delete an existing user
3. Log in
4. Log out
5. Add a new product
6. Delete an existing product
7. List all products
8. Purchase a product
9. Update Profile
10. View Order History
11. Search Products
12. Filter Products
13. Add to Cart
14. View Cart
15. Remove from Cart
16. Checkout
17. Exit

Please enter your choice (1-17):
```

### Example Console Interaction for New Features

#### Update Profile
```plaintext
Enter new email address:
Enter new delivery address:
[Success/Error message]
```

#### View Order History
```plaintext
Order History:
Order ID: 001, Product: Widget, Quantity: 2, Date: 2023-07-15, Total Cost: $39.98
Order ID: 002, Product: Gadget, Quantity: 1, Date: 2023-07-20, Total Cost: $29.99

Press Enter to return to the main menu.
```

#### Search Products
```plaintext
Enter product name to search: Widget
Search Results:
Product ID: 001, Name: Widget, Price: $19.99, Stock: 10

Press Enter to return to the main menu.
```

#### Filter Products
```plaintext
Enter minimum price: 10
Enter maximum price: 30
Filter Results:
Product ID: 001, Name: Widget, Price: $19.99, Stock: 10
Product ID: 002, Name: Gadget, Price: $29.99, Stock: 5

Press Enter to return to the main menu.
```

#### Add to Cart
```plaintext
Enter product ID to add to cart: 001
Enter quantity: 2
[Success/Error message]
```

#### View Cart
```plaintext
Shopping Cart:
Product ID: 001, Name: Widget, Quantity: 2, Total Cost: $39.98

Press Enter to return to the main menu.
```

#### Remove from Cart
```plaintext
Enter product ID to remove from cart: 001
[Success/Error message]
```

#### Checkout
```plaintext
Checking out...
Order Summary:
Product ID: 001, Name: Widget, Quantity: 2, Total Cost: $39.98

Order placed successfully! Your Order ID is 003.

Press Enter to return to the main menu.
```

### Detailed Workflow for New Features

1. **User Profile Management:**
   - **Update Profile:**
     - User selects the option to update their profile.
     - Prompt for new email and delivery address.
     - Update the user profile and provide feedback.
   - **View Order History:**
     - User selects the option to view order history.
     - Display all past orders with details.

2. **Product Search and Filtering:**
   - **Search Products:**
     - User selects the option to search products.
     - Prompt for product name or keyword.
     - Display matching products.
   - **Filter Products:**
     - User selects the option to filter products.
     - Prompt for minimum and maximum price.
     - Display products within the specified price range.

3. **Shopping Cart:**
   - **Add to Cart:**
     - User selects the option to add to cart.
     - Prompt for product ID and quantity.
     - Add the product to the cart and provide feedback.
   - **View Cart:**
     - User selects the option to view the cart.
     - Display all items in the cart with details.
   - **Remove from Cart:**
     - User selects the option to remove from cart.
     - Prompt for product ID.
     - Remove the product from the cart and provide feedback.
   - **Checkout:**
     - User selects the option to checkout.
     - Validate stock and update inventory.
     - Generate order ID and record the order.
     - Clear the cart and provide confirmation.
