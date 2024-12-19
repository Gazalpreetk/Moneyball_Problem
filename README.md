# Basketball Analytics, Moneyball

Situation: Oakland A's, a small-market team with limited financial resources, faced constant player losses to wealthier franchises.

Strategy: Billy Beane's innovative approach involved data-driven player evaluation using Sabermetrics, focusing on objective metrics like OBP and SLG.

# Moneyball Optimization Solution

# Objective:
To construct a baseball team that maximizes the total Wins Above Replacement (WAR) while staying under a $200 million salary cap and including at least 5 of the top players in terms of runs scored.

# Data:
The player data includes statistics such as At Bats (AB), Runs (R), Hits (H), Average (AVG), Home Runs (HR), WAR, and Salary among others. Each player's position is also taken into account to ensure a complete team roster is formed.

# Method

We used Microsoft Excel's Solver with the following setup:

Objective:   Maximize cell J$84 (total WAR of the selected team).

Variable Cells:   Z$2:Z$82 (binary decision variables indicating whether a player is chosen).

Constraints:

1. Total salary ≤ $200 million (K$84 ≤ 200)
2. At least 5 top players w.r.t runs included (L$85:L$85 ≥ L$86:L$86)
3. Decision variables are binary (Z$2:Z$82 = binary)
4. Exactly 15 players must be selected (Z$84 = 15)

![image](https://github.com/user-attachments/assets/5c52154a-e55d-48b9-a1be-d8af2c1dd0a4)


# Solver Configuration
Solving Method: GRG Nonlinear, as the problem is nonlinear due to the salary cap and minimum player conditions.
Results
The solver successfully found a team composition within the set constraints. The chosen team has a total WAR of 99.1 and total salary of $184.825 million.

# Selected Team Roster
The final team comprises the following players:

Aaron Judge | NYY | RF

Alejandro Kirk | TOR | C

Andres Gimenez | CLE | SS

Austin Riley | ATL | 3B

Brandon Nimmo | NYM | CF

J.T. Realmuto | PHI | C

Jeff McNeil | NYM | 2B

Julio Rodriguez | SEA | RF

Manny Machado | SD | 3B

Mookie Betts | LAD | RF

Nolan Arenado | STL | 3B

Paul Goldschmidt | STL | 1B

Tommy Edman | STL | 2B

Xander Bogaerts | BOS | SS

Yordan Alvarez | HOU | DH

# Analysis: 

This roster was selected for its high cumulative WAR, indicating a strong overall contribution above replacement-level players, while still meeting the salary and top player constraints. Notably, this selection strategy emphasizes performance metrics over traditional scouting methods, aligning with the Moneyball philosophy.


