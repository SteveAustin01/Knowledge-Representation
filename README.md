Knowledge Representation
Clue-Style Logical Reasoning Game in Python
This project showcases a Clue-style logical deduction game that utilizes propositional logic. It incorporates principles from AI Knowledge Representation and Logical Reasoning to model and resolve the game's mysteries. A dedicated logic.py module is employed to define symbols and sentences, enabling the program to perform logical inferences to ascertain the potential outcomes of the game.

Table of Contents
Overview
Installation
How It Works
Code Structure
Examples
Future Work
License
Overview
This project simulates a straightforward Clue-style game where the AI must deduce:

The character responsible for the crime
The location where the crime occurred
The weapon that was utilized
The game's rules and facts are framed in propositional logic, allowing the AI to make inferences and solve the puzzle. The project is designed to be adaptable, enabling it to tackle various logic-based challenges beyond this scenario.

![alt text](image.png)
How It Works
Knowledge Representation: The game leverages propositional logic to represent characters, locations, and weapons as symbols. Game rules and facts are encoded as logical sentences.
Logical Reasoning: The model_check function assesses whether the knowledge base supports specific queries. It employs a brute-force methodology to evaluate all possible models for logical entailment.
Constraints and Inference: The program ensures that all game rules are upheld while making inferences to unravel the puzzle.
Key Concepts
Symbols: These denote game elements (e.g., Colonel Mustard, Kitchen, Knife).
Sentences: Logical expressions that utilize symbols and logical operators (e.g., And, Or, Not).
Model Checking: A technique used to confirm if the knowledge base implies a given query, facilitating logical deductions.
Code Structure
main.py: The primary script responsible for initializing the game and executing logical reasoning.
logic.py: Contains classes for representing logical symbols and sentences, including operations such as And, Or, Not, Implication, and Biconditional.
README.md: Documentation outlining the project's details.
Examples
Here are some instances of how the game logic is established:

Defining Symbols:

mustard = Symbol("ColMustard")
kitchen = Symbol("kitchen")
knife = Symbol("knife")

Building the Knowledge Base:

knowledge = And(
Or(mustard, plum, scarlet), # At least one character is implicated
Or(ballroom, kitchen, library), # At least one room is implicated
Or(knife, revolver, wrench) # At least one weapon is implicated
)

Incorporating Constraints:

knowledge.add(Not(mustard))
knowledge.add(Not(kitchen))
knowledge.add(Not(revolver))
Verifying Knowledge:

python
check_knowledge(knowledge)
Future Work
Extend the game to include additional characters, rooms, and weapons.
Implement optimization methods for the model-checking process.
Develop a graphical user interface (GUI) for an enhanced user experience.
Integrate more intricate logical puzzles and scenarios.
