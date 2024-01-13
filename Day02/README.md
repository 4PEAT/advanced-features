
---

# Enhanced Payment Processing System

## Objective
Expand the `PaymentProcessor` interface in Java to include additional functionality and state management. Implement `CreditCardProcessor` and `PayPalProcessor` classes, each maintaining its own state and handling payments accordingly.

## Task Description

### 1. Interface Definition - `PaymentProcessor`
Implement the `PaymentProcessor` interface with the following specifications:

- **Abstract Method**:
  - `boolean processPayment(double amount)`: Process a payment of the specified amount. Return `true` if successful, and `false` if it fails.
- **Static Method**:
  - `static double convertCurrency(double amount, double exchangeRate)`: Convert the specified amount to another currency using the given exchange rate. Return the converted amount.
- **Default Method**:
  - `default void logTransaction(String transactionDetails)`: Log the transaction details with a timestamp.

### 2. Implementation Classes with Variables

- **`CreditCardProcessor` Class**:
  - Variables: `String cardType`, `double transactionFee`.
  - The `processPayment` method should consider the `transactionFee` for each transaction.
- **`PayPalProcessor` Class**:
  - Variables: `String accountEmail`, `boolean internationalPaymentsEnabled`.
  - The `processPayment` method should handle international payments based on the `internationalPaymentsEnabled` flag.

### 3. Main Class
Create a `Main` class to:
  - Instantiate and configure `CreditCardProcessor` and `PayPalProcessor`.
  - Process payments using both processors.
  - Utilize `convertCurrency` for currency conversions.
  - Log transactions using the `logTransaction` method.

## Additional Challenges
- Implement validations in the `processPayment` methods based on the state variables.
- Format the timestamp in the `logTransaction` method into a human-readable date and time.

## Requirements
- Implement state management in the `CreditCardProcessor` and `PayPalProcessor` classes.
- Showcase the use of abstract, static, and default methods in the interface.
- Handle various payment scenarios, reflecting the state of each processor.

## Expected Outcome
- A system where each processor has its configuration and state, influencing payment processing.
- Demonstrated ability to manage state within classes implementing an interface.
- Understanding of combining static and instance-specific behaviors.

