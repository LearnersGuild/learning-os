# Process: Project Creation

## Context

At the beginning of a cycle is a [Goal Selection](goal-selection.md) process followed by Project Creation. Project Creation kicks in when a cycle's vote cutoff time arrives.

## Purpose

Creating a project is a necessary step for players to begin working together as a team on a specific goal.

## Participants

- **Free Players**: players who are not currently on a project.

## Requirements

Every project team must meet the following requirements:

- Each Team Member's experience and skill level should be approximately equal
- No team should be without a Lead
- Team Members can only be on one team
- Teams should have no fewer than 3 and no more than 5 players (including Team Lead)
- A Team Lead cannot lead more than 3 teams
- Teams with a mean ECC of 30 or more do not need a Team Lead.

### Team Lead Requirements

A Team Lead must have an ECC of at least TEAM_LEAD_THRESHOLD cycles more than the mean of the Team Members' ECC. Use the Lead-Member Contribution Difference (LCMD) to calculate this.

Formula: LCMD >= TEAM_LEAD_THRESHOLD

A Team Lead may lead more than one team, so long as the following formula remains true:

Formula: aggregate LCMD for all teams >= <no teams leading> * TEAM_LEAD_THRESHOLD

Examples:
- If a Team Lead is assigned to two teams their ECC must be higher than the mean of all their teams' MECC by (2 * TEAM_LEAD_THRESHOLD), or 20 cycles.
- If a Team Lead is assigned to three teams their ECC must be higher than the mean of all their teams' MECC by (3 * TEAM_LEAD_THRESHOLD), or 30 cycles.

### Optimize for the following in order

1. Team leads should be on as few teams as possible
- All Free Players' Lead to Membership Ratio (LMR) should be as close to Target LMR as possible
- Assign as many players as possible to Goals they have voted for. Maximize Preferred Goal Selection Percentage (PGSP).
- Prefer teams of 4 players, followed by 5, followed by 3

## Steps

To form a team, complete steps 1 and 2. Repeat until all free players have been assigned to a team.

### Inputs

- Goals from goal selection process
- Player votes on the goals (each goal has at least MIN_TEAM_SIZE interested)
- Player stats (ECC, LMR, and PGSP)

### Step 1: Select Team Members and create Project

- Order all free players in ascending order of ECC, followed by descending order LMR, followed by ascending order PGSP
  - This way, the first player in the list has the least ECC, the highest LMR, and the lowest PGSP, i.e. the least experienced free player who has worked on the goals they voted for the least amount of times
- Pick the first free player on the list
- Of the Goals this free player voted for, pick the one that has the most votes
  - Create a Project from this Goal
  - Create a Team and assign this player to it
  - Assign the Team to the Project
- Of the _other_ free players that voted for this Goal, rate them ascending by PGSP and select the top (TARGET_TEAM_SIZE - 1)
- If team size is still less than MIN_TEAM_SIZE
  - Order free players by proximity to team MECC, followed by descending order LMR, followed by descending order PGSP
    - This way, we pick players who have the closest ECC to the rest of the team, who have higher lead:member ratios, and who have worked on goals of their choosing most often
  - Select free players from the top of that list until you've reached MIN_TEAM_SIZE
- Team now has all Team Members; for each of these Members:
  - Update their PGSP
  - Remove their votes from this goal and other goals they have voted for in this cycle
- Calculate the MECC for the selected Team Members from Step 1
- If MECC is more than (TEAM_LEAD_THRESHOLD * 3) skip Step 2 and repeat Step 1 until team is TARGET_TEAM_SIZE
  - Teams with high MECC don't need Team Lead

### Step 2: Select Team Leads

- Filter out any free players whose LMCD is < 5 cycles when compared to the team MECC
- If there are no free players on the list (we ran out of team leads)
  - Clear all teams, reset votes, and restart team formation process, this time with MIN_TEAM_SIZE increased by 1
- Order all free players in ascending order of ECC, followed by ascending order LMR, followed by descending order PGSP
  - This way, we choose Team Leads from free players with more experience than the team (but not too much more) who have the lowest lead:member ratios and have worked on their chosen goals the most
- Assign the first free player as Team Lead for this team
- Update their PGSP
- Remove that player's votes from this goal and other goals they have voted for in this cycle
- Loop back to Step 1 until all free players have been assigned to a team

## Stats Impacted
- PGSP

## Results
- Teams formed around Projects
