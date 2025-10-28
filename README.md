Project 1: RPG Character Creator

This project is a Python-based command-line application that allows users to create, save, load, and manage simple characters for a role-playing game (RPG).

Game Concept

The world is a classic fantasy setting where adventurers can belong to one of four classes: Mage, Warrior, Rogue, or Cleric. This application serves as the foundation for an RPG, allowing a player to create a new character, assign them a name and class, and generate their starting statistics.

Characters begin at Level 1 with 100 gold. They can be saved to a text file to persist between sessions and loaded back into the game later. The system also supports a level_up feature that increases a character's level and improves their stats, showing progression.

Design Choices

The core design revolves around the calculate_stats function, which determines a character's abilities based on their class and level.

Class-Based Stat Specialization

Base stats at Level 1 are designed to give each class a unique feel:

Warrior: High Strength (15) and Health (100), but low Magic (5). Designed to be a durable melee fighter.

Mage: High Magic (15) and medium Health (80), but very low Strength (5). Designed to be a powerful but fragile spellcaster.

Rogue: Balanced Strength (10) and Magic (10), but low Health (70). A "jack-of-all-trades" character.

Cleric: High Magic (12) and Health (90), with medium Strength (8). A hybrid class that can heal and withstand combat.

Stat Scaling Formula

To ensure characters grow stronger as they level up, a simple linear scaling formula is applied on top of the base stats:

Strength: Base Strength + (Level * 2)

Magic: Base Magic + (Level * 1)

Health: Base Health + (Level * 10)

This formula is applied universally to all classes. This means that while all characters get stronger, their core class specialization (e.g., a Warrior's high strength) is maintained and amplified as they level.

Bonus Creative Features

Level Up System: Includes a level_up function that not only increments the character's level but also automatically recalculates their stats based on the scaling formula.

Human-Readable Save Files: The save_character function saves data in a simple .txt file with clear key-value pairs (e.g., Class: Mage). This makes it easy to read, debug, or even manually edit character files outside of the game.

Four-Class System: Implements four distinct classes (Warrior, Mage, Rogue, Cleric), providing a solid foundation for different playstyles.

AI Usage

AI was used to make this README.md file, as well as help debugging the load_character() function to properly read the file's content and parse it to re-create the dictionary.

How to Run

This is a Python script and can be run from any terminal that has Python 3 installed.

Save the code as project1_starter.py.

Open your terminal or command prompt.

Navigate to the directory where you saved the file.

Run the script using the following command:

python project1_starter.py


Running the file directly will execute the test code located in the if __name__ == "__main__": block. This test will:

Create a "TestHero" of the "Warrior" class.

Display the new character's sheet.

Save the character to my_character.txt.

Load the character from the file.

Level up the character to Level 2.

Display the character's updated sheet with new stats.