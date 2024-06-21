### Task: Build a Reflection-Based Configuration Loader

#### Background
In many applications, there is a need to load configurations dynamically at runtime without hard-coding values. These configurations could be for various aspects such as database settings, API keys, or operational parameters. The objective is to use Java reflection to load these settings into Java objects from a simulated external source (for this exercise, hardcoded values).

#### Requirements

1. **Create a Configurable Object**:
    - Design a Java class named `AppConfig` that contains several settings such as `databaseUrl`, `maxConnections`, `apiToken`, and `featureEnabled` with various data types (`String`, `int`, `String`, `boolean`).

2. **Load Configuration Dynamically**:
    - Write a method `loadConfiguration(Object configObject)` in a `ConfigurationLoader` class that dynamically assigns values to the respective fields in the `AppConfig` object using reflection.

      - **Detailed Steps**:
          1. **Simulate the Configuration Source**:
              - Hardcode the configuration values directly within the `loadConfiguration` method. These values should correspond to the fields in the `AppConfig` class.
          
          2. **Access Fields Using Reflection**:
              - Use reflection to iterate over the fields of the `configObject`.
              - Ensure each field is accessible for modification.
          
          3. **Match Field Names and Assign Values**:
              - For each field in the `configObject`, match the field name with the hardcoded configuration values.
              - Convert the hardcoded value to the appropriate type required by the field.
          
          4. **Assign the Value to the Field**:
              - Use reflection to set the field value in the `configObject`.
          
          5. **Handle Errors**:
              - Implement error handling for potential issues such as:
                - The field not being found in the `configObject`.
                - Type mismatches when converting hardcoded values.
                - Exceptions during reflection operations.

3. **Handling Different Field Types**:
    - Ensure the loader correctly handles different data types and converts values from the hardcoded source into appropriate types for the fields (e.g., converting a string "10" to an integer for `maxConnections`).

4. **Display Configurations**:
    - After loading the configurations, the program should print out all the field values of the `AppConfig` instance to confirm that values have been set correctly.

#### Expected Deliverables

1. **Java Class Definitions**:
    - Define the `AppConfig` class with appropriate fields and types.
    - Define a `ConfigurationLoader` class with a method `loadConfiguration(Object configObject)`.

2. **Main Class for Execution**:
    - A `Main` class that creates an instance of `AppConfig`, invokes the configuration loader, and prints the loaded configurations.

3. **Error Handling**:
    - Include basic error handling for issues like missing fields, type mismatches, and exceptions that may occur during reflection operations.

#### Example of Expected Operation
```java
public static void main(String[] args) {
    AppConfig config = new AppConfig();
    ConfigurationLoader loader = new ConfigurationLoader();
    loader.loadConfiguration(config);
    System.out.println(config);
}
```

This task will help you practice using Java reflection to dynamically load configuration values into an object, handle various data types, and ensure the configuration values are correctly assigned and displayed.
