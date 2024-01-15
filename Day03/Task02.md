### Task: Implement Validations in Java Classes

#### Objective
Create two Java classes, `Person` and `Calculator`, with specific validation rules. Your task is to ensure these classes handle invalid inputs correctly by throwing an `IllegalArgumentException`.

#### Task Details

**1. Validating the `Person` Class**
- **Constructor Requirements**:
  - The `Person` class should have a constructor that accepts two parameters: `name` (String) and `age` (int).
  - Implement validation in the constructor:
    - The `name` should not be null, empty, or over 40 characters in length.
    - The `age` should be between 0 and 120 (inclusive).
  - If the input parameters do not meet these criteria, the constructor should throw an `IllegalArgumentException` with an appropriate error message.

**2. Validating the `Calculator` Class**
- **Method Requirements**:
  - Implement a `factorial` method:
    - The method should accept an integer and return its factorial.
    - It should only process non-negative numbers (0 or greater). If a negative number is passed, throw an `IllegalArgumentException`.
  - Implement a `binomialCoefficient` method:
    - The method should accept two integers, `n` (set size) and `k` (subset size), and return the binomial coefficient (_nCk_).
    - Ensure both `n` and `k` are non-negative, and `k` does not exceed `n`. If these conditions are not met, throw an `IllegalArgumentException`.

#### Implementation Notes
- Handle exceptions gracefully and provide clear error messages for the user.
- Include comments in your code to explain your logic.
- Ensure your code is clean and follows Java coding standards.

