### Task: Develop a Java OOP Game System

#### Overview
You are tasked with creating a console-based role-playing game (RPG) in Java. This game should showcase the fundamental principles of OOP: Encapsulation, Inheritance, Polymorphism, and Abstraction.

#### Task Details

**1. Encapsulation: Character and Item Management**
   - **Character Class**: Create a `Character` class with private attributes (e.g., `name`, `health`, `strength`). Implement public methods for data access and manipulation.
   - **Item Class**: Create an `Item` class to represent various items in the game. Each item should have attributes like `name`, `type`, and `effect` encapsulated within it.

**2. Inheritance: Character Specialization**
   - Develop subclasses (e.g., `Warrior`, `Mage`, `Archer`) that inherit from `Character`. Each subclass should have unique properties and behaviors.
   - Implement a method in each subclass that reflects its unique skill or ability.

**3. Polymorphism: Special Abilities**
   - Introduce a polymorphic method `performSpecialMove()` in the `Character` class. This method will be overridden in each subclass to perform a character-specific special move.

**4. Abstraction: Battle Mechanics**
   - Design an interface `Battle` with methods like `startFight(Character, Character)`, `attack(Character, Character)`, and `defend(Character)`.
   - Implement this interface in a `SimpleBattle` class that outlines the basic battle mechanics between characters.

**5. Game Flow Implementation**
   - Create a `Game` class to handle the overall game mechanics. This includes character creation, item management, and initiating battles.

**6. Demonstration and Testing**
   - In the `main` method of the `Game` class, demonstrate the creation of different characters and items.
   - Simulate a battle scenario to showcase how different characters use their special abilities.
   - Highlight the use of OOP concepts: Create characters (encapsulation), use subclass specific methods (inheritance and polymorphism), and initiate a battle (abstraction).

#### Deliverables
- Source Code: Complete Java source code with comments explaining the OOP concepts.
- Documentation: A README file describing the game mechanics, how to run the game, and an overview of the OOP concepts implemented.

#### Bonus Challenges
- Add an inventory system for characters to hold multiple items.
- Implement more complex battle mechanics considering attributes like defense, speed, and item effects.
- Introduce a simple storyline where characters can engage in multiple battles and quests.

This task is designed to provide a comprehensive understanding of OOP principles through a practical, engaging project. It allows for creativity in expanding game features while focusing on solidifying your understanding of Java OOP concepts.
