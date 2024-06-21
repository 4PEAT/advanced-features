### Task: Build a Reflection-Based Configuration Loader

#### Background
In many applications, there is a need to load configurations dynamically at runtime without hard-coding values. These configurations could be for various aspects such as database settings, API keys, or operational parameters. The objective is to use Java reflection to load these settings into Java objects from a simulated external source (for this exercise, hardcoded values or a properties file).

#### Requirements

1. **Create a Configurable Object**:
    - Design a Java class named `AppConfig` that contains several settings such as `databaseUrl`, `maxConnections`, `apiToken`, and `featureEnabled` with various data types (`String`, `int`, `String`, `boolean`).

2. **Load Configuration Dynamically**:
    - Write a method `loadConfiguration(Object configObject)` in a `ConfigurationLoader` class that reads a properties file (simulated by hardcoded values in a `Map` for this exercise) and dynamically assigns these values to the respective fields in the `AppConfig` object using reflection.

3. **Handling Different Field Types**:
    - Ensure the loader correctly handles different data types and converts string values from the configuration source into appropriate types for the fields (e.g., converting a string "10" to an integer for `maxConnections`).

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
