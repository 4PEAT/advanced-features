### Task: Develop a Java OOP Role-Playing Game

#### Objective
Design and implement a console-based role-playing game in Java to illustrate the core concepts of Object-Oriented Programming: Encapsulation, Inheritance, Polymorphism, and Abstraction.

#### Task Breakdown

**1. Encapsulation: Character and Item Management**
   - **Character Class**: Develop a `Character` class with private attributes like `name`, `health`, `strength`. Include public methods for data access and manipulation.
   - **Item Class**: Create an `Item` class for game items. Each item should have private attributes `name`, `type`, `effect`, and a method to apply its effect to a character.

**2. Inheritance: Character Specialization**
   - Develop subclasses of `Character` (e.g., `Warrior`, `Mage`, `Archer`) with unique properties and behaviors.
   - Implement at least one unique method in each subclass that reflects its specialization.

**3. Polymorphism: Special Abilities**
   - Implement a polymorphic method `performSpecialMove()` in the `Character` class.
   - Override this method in each subclass for a character-specific special move.

**4. Abstraction: Battle Interface**
   - Design a `Battle` interface with methods like `startFight(Character, Character)`.
   - Implement the interface in a `SimpleBattle` class to define the basic rules of engagement between characters.

**5. Game Flow Implementation**
   - Create a `Game` class to manage the game. It should handle character creation, item management, and initiating battles.

**6. Demonstration and Testing**
   - In the `main` method of `Game`, demonstrate character creation, item usage, and a battle simulation.
   - Showcase encapsulation by interacting with character and item properties through their methods.
   - Demonstrate inheritance and polymorphism through subclass-specific methods and special moves.
   - Use the `Battle` interface to initiate a battle, illustrating abstraction.

#### Deliverables
- Complete Java source code with comments explaining the implementation of OOP concepts.
- A README file providing an overview of the game mechanics, how to run the game, and an explanation of the OOP concepts used.

#### Advanced Challenges (Optional)
- Enhance the battle system with additional features like defense, speed, and more complex item effects.
- Implement an inventory system where characters can carry multiple items.
- Create a simple storyline where characters go through multiple levels or quests.
