# Process: Team Formation

TODO: replace BD with EC

## Context

At the beginning of a cycle is a [Goal Selection](goal-selection.md) process followed by Team Formation. Team Formation kicks in when a cycle's vote cutoff time arrives.

## Purpose

Forming a team is a necessary step for players to begin working on a goal.

## Participants

- **Free Agents**: players who are not currently on a team.

## Requirements

Every team must meet the following requirements:

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
- If a Team Lead is assigned to two teams their ECC must be higher than the mean of all their Team Members' ECC by (2 * TEAM_LEAD_THRESHOLD), or 20 cycles.
- If a Team Lead is assigned to three teams their ECC must be higher than the mean of all their Team Members' ECC by (3 * TEAM_LEAD_THRESHOLD), or 30 cycles.

### Optimize for the following in order

1. Team leads should be on as few teams as possible
- All Free Agents' Lead to Membership Ratio (LMR) should be as close to Target LMR as possible
- Assign as many players as possible to Goals they have voted for. Maximize Preferred Goal Selection Percentage (PGSP).
- Prefer teams of 4 players, followed by 5, followed by 3

## Inputs

- Goals from goal selection process
- Player votes on the goals (each goal has at least 3 players interested)
- Player stats (Build Days and LMR)

## Steps

### Step 1: Select Team Members and create Goal Instances

- TEAM_MEMBERS_SIZE_TARGET = 3
- Order all players in ascending order of Effective Contribution, followed by ascending order LMR, followed by ascending order PGSP
- Pick the first player on the list (this is the least experienced player who has worked on the goals they voted for the least amount of times)
- Of the Goal Templates this player voted for, pick the one that has the most votes.
  - Create a Goal Instance off of that template
  - Create a Team and assign this player to it
  - Assign the Team to the Goal Instance
- Of the _other_ players that voted for this Goal Template, rate them ascending by PGSP and select the top (TEAM_MEMBERS_SIZE - 1)
- If you didn't get enough players from the previous step to reach TEAM_MEMBERS_SIZE
  - Find the 10 players who are not yet on a team who are closest to this teams average Effective Contribution
  - Order these players ascending by LMR followed by PGSP
  - Select to the top players from that list until you've reached TEAM_MEMBERS_SIZE
- You now have TEAM_MEMBERS_SIZE team members, for each of these members:
  - Update their PGSP
  - Remove their votes from this goal and other goals they have voted for in this cycle
- Calculate the average Effective Contribution (EC) for the selected Team Members from Step 1
- If average is more than 30 skip Step 2 and repeat step 1

### Step 2: Select Team Leads

- Order all players in ascending order of Total Contribution, followed by descending order LMR, followed by descending order PGSP
- Filter out any players whose Build Days is less than 50 higher than than the Team Members' average BD
- Filter out any players whose LMR is less than 3
- If there are still players on the list
  - Assign the first player as Team Lead with the Team Members
  - Remove that player's votes from this goal and other goals they have voted for in this cycle
  - Loop back to Step 1 until all players have been assigned a goal and a team
- Else (we ran out of team leads)
  - Reset all teams, goals, and votes, and redo the whole process, this time with TEAM_MEMBERS_SIZE increased by 1



## Stats Impacted
- PGSP

## Results
- Teams formed around Goal Instances


TODO: Order by total contribution not build days
TODO: More plain english here in steps
TODO: Simplify the algorithm
