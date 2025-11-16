# Scrooge's Bonus

A themed gift-exchange game inspired by A Christmas Carol. The employer (Scrooge) chooses between turkey or no_turkey each round, and employees choose high or low effort. Payoffs follow a standard gift-exchange matrix.

## Quick start

- Open and run run_game.ipynb to configure strategies and rounds, then view the actions and scores tables plus a leaderboard.
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


