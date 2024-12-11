# AI-Policy

## Description 

This project implements a bot using the concept of a Policy (a function that returns an action to perform based on the current state of the system).  
To create the Policy, the following steps are performed:
- First, a dataset is generated by recording player experiences (using a bot that performs random actions).
- Next, average values for tuples are computed, and these values are used to select the actions that maximize the score.

The tests conducted for this project are based on the game 421.

421 is a dice game where players aim to achieve specific combinations to win.
Players have a limited number of attempts to reach the winning combination and can choose between two actions for each die:
- `Keep`: Keep the current value of the die.
- `Roll`: Roll the die for a new value.   

For example, with 3 dice showing the roll `3 2 6`, the player might aim to achieve 
the winning combination `4 2 1`. In this case, the action to perform could be `roll keep roll`.

#### Project Feature

This project allows you to represent three types of players:
1. `Policy Bot`: A bot that makes decisions based on a predefined policy.
2. `Random Bot`: A bot that takes random actions during gameplay.
3. `Human Player`: A mode where you can directly play the game.

#### Directory Structure:

- `src`: Contains the source code of the project.
- `data`: Includes the game configuration file.
- `game`: Game class.
- `player`: Contains the implementations of the three types of players: Policy, Random, and Human.

## Results

Because it is a game of chance, it is not possible to predict the outcome of a game with precision. 
However, it is possible to optimize the score.
The scoring system is as follows:
- Winning combination → 100 points
- All the dice show the same value:
  - If the value is 1 → 30 points
  - Otherwise → 25 points
- All the dice show 1, except for one → 10 points 
- A sequence of consecutive numbers → 20 points
- Any other combination → 1 point

Using a Random Bot to play 10,000 games, the following results were obtained:
```
690 games won 
9310 games lost
score: 4.598266/100
```

Using a Policy Bot to play 10,000 games, the following results were obtained:
```
1466 games won 
8534 games lost
score: 9.096966/100
```

## Requirement

- Having Python3 and Pip installed on your machine.

## Execution 

To get the project running on your machine, you can run the `installation-requirements.sh` script to install the `venv` environment.  

Once the prerequisites are installed, you can run the `launcher.sh` script to execute the project.  
Follow the project instructions and have fun :)  

### On Ubuntu:

To execute a `.sh` Script:  
   1. Open a terminal.  
   2. Run the command `chmod +x script_name.sh` to make the script executable.  
   3. Execute the script by running `./script_name.sh`.  

Commands to run to make the project work:
1. Cloning the project to your machine
```sh
git clone https://github.com/AlexisEgea/AI-Policy.git
```
2. Installing the prerequisites
```sh
chmod +x installation-requirements.sh
```
```sh
./installation-requirements.sh
```
3. Run the project
```sh
chmod +x launcher.sh
```
```sh
./launcher.sh
```

### On Windows:

Double-click on the `installation-requirements.sh` script, preferably with `Git Bash`, to install the prerequisites:
```
installation-requirements.sh
```

Double-click on the `launcher.sh` script, preferably with `Git Bash`, to run the project:
```
launcher.sh
```
---

Note that the current version of the project has been tested on both Linux and Windows (Git Bash). If you encounter difficulties running the project, feel free to use an IDE (PyCharm, VS Code, or another), create a `venv` environment and execute the one of the `launcher_bot.py` file depending on the player you want to use.

## Contact Information

For inquiries or feedback, please contact me at [alexisegea@outlook.com](mailto:alexisegea@outlook.com).

## Copyright

© 2024 Alexis EGEA. All Rights Reserved.

