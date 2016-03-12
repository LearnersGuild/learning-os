# Process: Team Formation

## Context

After a cycle starts, and before the next cycle begins there is a process of [Goal Selection](goal-selection.md) followed by Team Formation. Team formation kicks in when a cycle's vote cutoff time arrives.

## Purpose

### Requirements
- Team experience and skill level should be approximately equal, with the exception of 1 player who should be more experienced and skilled (Team Lead)
- No team should be without a lead
- Team members can only be on one team
- Teams should be no fewer than 3 and no more than 5 players
- <no teams leading> * 50 >= <my BD> - <avg team BD>
  - A Team Lead's Build Days (BD) should be higher than their Team Members' average BD by 50 (10 weeks)
  - If a Team Lead is assigned to two teams their BD should be higher than their Team Members' average BD by 100 (20 weeks)
  - If a Team Lead is assigned to three teams their BD should be higher than their Team Members' average BD by 150 (30 weeks)
- A Team Lead should not belong to more than 3 teams
- Teams with an average BD of 150 or more don't need a team lead

TODO: Simplify formula above

### Optimize for the following in order
- Team leads should be on as few teams as possible
- Players Lead to Membership Ratio (LMR) should be as close to 3 as possible
- Assign as many players as possible to Goals they have voted for. Maximize Preferred Goal Selection Percentage (PGSP).
- Prefer teams of 4 players, followed by 5, followed by 3


## Inputs

- Goals from goal selection process
- Player votes on the goals (each goal has at least 3 players interested)
- Player stats (Build Days and LMR)

## Steps

### Step 1: Select Team Members and create Goal Instances

- TEAM_MEMBERS_SIZE_TARGET = 3
- Order all players in ascending order of Build Days, followed by ascending order LMR, followed by ascending order PGSP
- Pick the first player on the list (this is the least experienced player who has worked on the goals they voted for the least amount of times)
- Of the Goal Templates this player voted for, pick the one that has the most votes.
  - Create a Goal Instance off of that template
  - Create a Team and assign this player to it
  - Assign the Team to the Goal Instance
- Of the _other_ players that voted for this Goal Template, rate them ascending by PGSP and select the top (TEAM_MEMBERS_SIZE - 1)
- If you didn't get enough players from the previous step to reach TEAM_MEMBERS_SIZE
  - Find the 10 players who are not yet on a team who are closest to this teams average Build Days
  - Order these players ascending by LMR followed by PGSP
  - Select to the top players from that list until you've reached TEAM_MEMBERS_SIZE
- You now have TEAM_MEMBERS_SIZE team members, for each of these members:
  - Update their PGSP
  - Remove their votes from this goal and other goals they have voted for in this cycle
- Calculate the average Build Days for the selected Team Members from Step 1
- If average is more than 150 skip Step 2 and repeat step 1

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
