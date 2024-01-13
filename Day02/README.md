
# Payment Processing System Task

## Objective
Develop a Java-based payment processing system with specific behaviors in the `processPayment` method for different payment processors.

## Detailed Task Instructions

### 1. PaymentProcessor Interface
- Implement the `PaymentProcessor` interface with the following methods:
  - **Abstract Method**: `boolean processPayment(double amount)`
  - **Static Method**: `static double convertCurrency(double amount, double exchangeRate)`
  - **Default Method**: `default void logTransaction(String transactionDetails)`

### 2. CreditCardProcessor Class
- Implement the `CreditCardProcessor` class with specific behaviors in `processPayment`:
  - Calculate a transaction fee based on a percentage of the amount (e.g., 2%).
  - Check if the sum of the transaction amount and transaction fee exceeds a predefined limit (e.g., $5000). If it does, the payment should fail.
  - Log a successful or failed transaction message using the `logTransaction` method, including details about the transaction amount and fee.

### 3. PayPalProcessor Class
- Implement the `PayPalProcessor` class with specific behaviors in `processPayment`:
  - Validate the email address associated with the PayPal account.
  - Apply a flat transaction fee (e.g., $2.00) for all PayPal transactions.
  - Log a successful or failed transaction message using the `logTransaction` method, including details about the transaction and the applied fee.

### 4. Main Class
- Demonstrate the functionality in a `Main` class:
  - Create instances of both `CreditCardProcessor` and `PayPalProcessor`.
  - Process payments with various scenarios (e.g., exceeding limits, applying fees).
  - Utilize the `convertCurrency` method for international transactions.
  - Log all transactions.

## Additional Challenges
- Implement error handling for invalid inputs or payment processing failures.
- Enhance the `logTransaction` method to include detailed transaction information and readable timestamps.

## Requirements
- Accurately implement the specified behaviors in the `processPayment` method for each class.
- Demonstrate the use of abstract, static, and default methods in the interface.
- Ensure proper handling of different payment processing scenarios.

## Expected Outcome
- A robust payment processing system capable of handling various scenarios, including transaction fees and limits.
- Clear demonstration of object-oriented principles and Java interface implementation.
