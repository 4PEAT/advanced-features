
### 1. Room and Hotel Structure

```java
// Abstract class representing a general room
abstract class Room {
    protected int roomNumber;
    protected double price;
    // Constructor, getters, and setters

    // Abstract method for calculating rate
    public abstract double calculateRate();
}

// Concrete class for a standard room
class StandardRoom extends Room {
    // Implementation of abstract methods and additional features specific to a standard room

    @Override
    public double calculateRate() {
        // Specific calculation for a standard room
        return price;
    }
}

// Interface for amenities
interface WifiAccessible {
    boolean hasWifiAccess();
}
```

### 2. Booking and Customer Management

```java
class Customer {
    private String name;
    private String email;
    private List<Booking> bookings;
    // Constructor, getters, and setters
}

class Booking {
    private Room room;
    private LocalDate startDate;
    private LocalDate endDate;
    // Constructor, getters, and setters
}
```

### 3. Reservation System

```java
class ReservationSystem {
    private List<Room> rooms = new ArrayList<>();
    private List<Booking> bookings = new ArrayList<>();

    public void addRoom(Room room) {
        rooms.add(room);
    }

    public void makeBooking(Booking booking) throws RoomNotAvailableException {
        // Check room availability and add booking
    }
}
```

### 4. Utility Services

```java
// Enumeration for room status
enum RoomStatus {
    AVAILABLE, OCCUPIED, UNDER_MAINTENANCE;
}

// Custom exception for handling booking errors
class RoomNotAvailableException extends Exception {
    public RoomNotAvailableException(String message) {
        super(message);
    }
}
```

### 5. User Interface and Interaction (Console-Based)

```java
import java.util.Scanner;

public class HotelBookingApp {
    private static ReservationSystem reservationSystem = new ReservationSystem();

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // Simplified console interaction loop
        while (true) {
            System.out.println("Welcome to the Hotel Booking System");
            // Implement menu options for adding rooms, making bookings, etc.
            // Use scanner to get input from user
            int choice = scanner.nextInt();
            switch (choice) {
                case 1:
                    // Add room
                    break;
                case 2:
                    // Make a booking
                    break;
                // Additional cases
                default:
                    System.out.println("Invalid option. Please try again.");
            }
        }
    }
}
```

### Sorting with Anonymous Class

As an example of using an anonymous class for sorting within this context:

```java
Collections.sort(rooms, new Comparator<Room>() {
    @Override
    public int compare(Room room1, Room room2) {
        return Double.compare(room1.getPrice(), room2.getPrice());
    }
});
```
