# Payment Processing System Task

## Objective
Develop a Java-based payment processing system with a focus on implementing detailed behaviors in the `processPayment` method for different payment processors.

## Detailed Task Instructions

### 1. PaymentProcessor Interface
- Implement the `PaymentProcessor` interface with the following methods:
  - **Abstract Method**: `boolean processPayment(double amount)`
  - **Static Method**: `static double convertCurrency(double amount, double exchangeRate)`
  - **Default Method**: `default void logTransaction(String transactionDetails)`

### 2. CreditCardProcessor Class
- Implement the `CreditCardProcessor` class with specific behaviors in `processPayment`:
  - Check if the transaction amount exceeds a predefined limit (e.g., $5000). If it does, the payment should fail.
  - Calculate a transaction fee based on a percentage of the amount (e.g., 2% of the transaction amount) and include this in the payment processing.
  - Log a successful or failed transaction message using the `logTransaction` method.

### 3. PayPalProcessor Class
- Implement the `PayPalProcessor` class with specific behaviors in `processPayment`:
  - Validate the email address associated with the PayPal account (e.g., check if it contains a domain name).
  - If `internationalPaymentsEnabled` is `true`, process international payments by applying an additional fee or exchange rate. Otherwise, limit transactions to domestic payments.
  - Log a successful or failed transaction message using the `logTransaction` method.

### 4. Main Class
- Demonstrate the functionality in a `Main` class:
  - Create instances of both `CreditCardProcessor` and `PayPalProcessor`.
  - Process payments with various scenarios (e.g., exceeding limits, international payments).
  - Utilize the `convertCurrency` method for international transactions.

## Additional Challenges
- Implement error handling for invalid inputs or payment processing failures.
- Enhance the `logTransaction` method to include detailed transaction information and readable timestamps.

## Requirements
- Accurately implement the specified behaviors in the `processPayment` method for each class.
- Demonstrate the use of abstract, static, and default methods in the interface.
- Ensure proper handling of different payment processing scenarios.

## Expected Outcome
- A robust payment processing system capable of handling various scenarios and providing detailed transaction logs.
- Clear demonstration of object-oriented principles and Java interface implementation.
