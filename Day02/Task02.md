### Task: Develop a Java OOP Role-Playing Game

#### Objective
Design and implement a console-based role-playing game in Java, demonstrating the core concepts of Object-Oriented Programming: Encapsulation, Inheritance, Polymorphism, and Abstraction.

#### Environment Setup
- Install Java SDK and an IDE (e.g., Eclipse, IntelliJ IDEA).
- Set up a Java project with an organized package structure.

#### Detailed Task Description

**1. Encapsulation: Character and Item Management**
   - **Character Class**: Create a `Character` class with private attributes (`name`, `health`, `strength`). Include methods to access and modify these attributes, ensuring data integrity.
   - **Item Class**: Develop an `Item` class representing game items, with private attributes (`name`, `type`, `effect`). Include a method `useItem(Character character)` that applies the item's effect to a character, such as increasing strength or health.

**2. Inheritance: Character Specialization**
   - Develop subclasses of `Character` (e.g., `Warrior`, `Mage`, `Archer`). Each subclass should have additional attributes or methods that are unique to its type.
   - For example, `Warrior` might have increased strength, while `Mage` could have a unique magical ability.

**3. Polymorphism: Implementing Special Abilities**
   - Implement a method `performSpecialMove()` in the `Character` class. This method will perform a generic action, like a standard attack.
   - Override `performSpecialMove()` in each subclass to execute a move unique to that character type, like a powerful sword strike for `Warrior` or a magic spell for `Mage`.

**4. Abstraction: Battle Mechanics**
   - Define an interface `Battle` with methods such as `startFight(Character, Character)`.
   - Implement this interface in a class, `SimpleBattle`, defining the basic rules and flow of a fight between two characters, like alternating attacks until one character's health reaches zero.

**5. Game Flow Implementation**
   - Create a `Game` class to manage the game mechanics. This includes creating characters, managing items, and initiating battles.

**6. Demonstration and Testing**
   - In the `Game` class's `main` method, demonstrate creating characters and items.
   - Simulate a battle to showcase special moves, item usage, and the battle process.
   - Clearly demonstrate encapsulation by interacting with objects through their methods, inheritance and polymorphism through the special moves of character subclasses, and abstraction by using the `Battle` interface.

#### Deliverables
- Full Java source code with comments explaining the implementation and OOP concepts.
- A README file describing game mechanics, instructions for running the game, and an overview of OOP concepts applied.

#### Bonus Challenges (Optional)
- Implement advanced battle mechanics (e.g., defense, speed, special conditions).
- Create an inventory system for characters.
- Develop a simple storyline with multiple levels or quests.
