# Scrooge's Bonus

## About the game

Scrooge's Bonus is based on the gift-exchange game (also known as the gift exchange dilemma), a common economic game theory model introduced by George Akerlof and Janet Yellen to simulate reciprocacy in labor relations. It serves as a valuable tool for understanding the principal-agent problem in labor economics.

Here is an overview of the gift-exchange game and its structure, providing context for the Scrooge's Bonus game:

While the simplest form of the general gift-exchange game typically involves only two players—an employer and an employee—the Scrooge's Bonus game, which is a themed implementation of the gift-exchange dilemma, uses a multi-player format for the ABS Data Engineers' Challenge. The game proceeds sequentially:
1. Employer's Move (The Gift): The employer first decides whether to award a bonus to the employee (the "turkey") or give no bonus.
2. Employee's Move (The Reciprocation): Employees then individually decide whether to reciprocate the bonus choice with a higher level of effort (work harder) or a lower level of effort.

This sequence continues for a number of rounds. 

The core concept the game investigates is reciprocity. The theory suggests that if the employer offers a higher salary, employees are more inclined to reciprocate with greater effort, leading to mutually beneficial outcomes. Reciprocity is a fundamental factor that shapes individuals' behavior in economic contexts, demonstrating that self-interest maximization is not the sole determinant of economic decision-making.

![Scrooge's Bonus](image.png)

## Quick start

- Open and run run_game.ipynb to select strategies and rounds, then view the actions and scores tables plus a leaderboard.
- Helpers live in game_helpers.ipynb. Sample strategies live in sample_players.ipynb.

## Core actions

- Employer actions: turkey, no_turkey
- Employee actions: high, low

## Payoff matrix (employer, employee)

- (turkey, high): (2, 2)
- (turkey, low): (0, 3)
- (no_turkey, high): (3, 0)
- (no_turkey, low): (1, 1)

## Build your own strategies

- Employer strategy signature: def employer(history: pd.DataFrame) -> str where history has columns employer_action, high_effort, low_effort.
- Employee strategy signature: def employee(history: pd.DataFrame) -> str where history additionally includes my_action.

Notes

- See sample_players.ipynb for simple baselines like generous and tit_for_tat.


