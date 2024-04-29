
### Task 1: Support More Data Types

**Objective:** 
Improve the flexibility of the configuration loader by expanding the range of data types it can handle, thus accommodating more complex configuration scenarios.

**Detailed Actions:**
1. **Extend Basic Data Type Support**:
   - **Double, Long, Float**: Enhance the `convertValue` method to include conversions from `String` to `double`, `long`, and `float`. Each conversion should handle any potential `NumberFormatException` to ensure the loader remains robust and error-tolerant.
AppConfig class can look like this
```java
public class AppConfig {
    private String databaseUrl;
    private int maxConnections;
    private String apiToken;
    private boolean featureEnabled;
    
    // New fields for additional data types
    private double performanceScore;   // to store values like system performance scores
    private long dataRetentionDays;    // to store values in days for data retention policies
    private float retryInterval;       // to store values like retry intervals in seconds

```
   - Implement error handling using try-catch blocks to catch conversion errors and provide meaningful error messages or default values in case of exceptions.

2. **Add Support for Date Type**:
   - **Date Conversion**: Implement conversion logic to parse strings into `Date` objects. Since date formats can vary, decide on a standard format (e.g., "yyyy-MM-dd") for your configurations.
   - Use `SimpleDateFormat` for converting the string to a `Date`. Wrap the parsing in a try-catch block to handle `ParseException`, and consider providing a fallback or error message if parsing fails.

**Considerations for Robust Implementation**:
- Ensure that the `convertValue` method clearly logs which type conversion failed if an error occurs, to aid in debugging.
- Consider allowing the configuration file to specify the date format dynamically, which could then be used in the parsing logic.

### Task 2: Configuration Validation

**Objective:** 
Establish a system to validate configuration values once they are loaded, ensuring they meet the defined criteria and thus maintaining the system's integrity and reliability.

**Detailed Actions:**
1. **Implement Validation Logic**:
   - **Method Setup**: Create a new method in `ConfigurationLoader` called `validateConfiguration`. This method should check each critical configuration parameter for validity after it has been set on the `AppConfig` instance.
   - **Specific Validations**: For `maxConnections`, ensure the value is a positive integer. For `databaseUrl`, ensure it conforms to a valid URL pattern. Implement these checks using standard Java functionality, like comparing integer values and using regex for URL validation.

2. **Use Annotations for Declarative Validation Rules**:
   - **Annotation Definitions**: Define custom annotations such as `@Min(value)` for numeric validations and `@URL` for string format validations. These annotations should be able to be placed directly on the fields in `AppConfig`.
   - **Processing Annotations**: Modify the `ConfigurationLoader` to inspect fields of `AppConfig` for these annotations and enforce the constraints during the loading process.
   - **Reflection Utilization**: Use reflection to read annotations from fields and determine if the loaded values meet the criteria specified by these annotations.

