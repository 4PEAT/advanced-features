### Task Description:

Write a program that simulates a parking garage management system. The system will handle multiple cars attempting to park and leave the garage simultaneously. If a car arrives and there are no available parking spots, it should wait until a spot becomes available. When a car leaves, any waiting cars should be notified and allowed to park.

**Requirements:**

1. **Parking Cars**: 
   - Implement multiple car threads that attempt to park in the garage.
   - If a parking spot is available, the car should park immediately.
   - If no parking spots are available, the car should wait until a spot is free.

2. **Leaving Parking Spots**: 
   - Cars should leave their parking spots after a random period of time.
   - When a car leaves, any waiting cars should be notified and allowed to park.

3. **Concurrency Control**:
   - Implement concurrency control to ensure that parking and leaving is thread-safe and that cars are correctly notified when spots become available.


### Explanation:

1. **ParkingGarage Class**:
   - Manages the available parking spots and a queue of waiting cars.
   - The `parkCar` method makes cars wait if no spots are available and notifies them when a spot is free.
   - The `leaveCar` method increases the number of available spots and notifies waiting cars.

2. **Car Class**:
   - Simulates a car attempting to park in the garage.
   - If a spot is available, the car parks and waits for a random period before leaving.
   - If no spot is available, the car waits until notified.

3. **ParkingGarageSimulation Class**:
   - Initializes the parking garage with a set number of spots.
   - Creates multiple car threads to simulate cars arriving at the garage.
