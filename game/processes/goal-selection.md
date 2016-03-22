# Process: Goal Selection

## Context

Goal selection is the first process in the [game cycle](cycle.md).
During goal selection, players indicate their commitment to participating in the cycle by voting for one or more Goal Templates.

## Purpose

The purpose of the Goal Selection process is to prepare for the Team Formation process by identifying:

- Players that are going to participate in the cycle
- Goal Templates these players are interested in
- Most popular Goal Templates for this cycle

Players indicate interest in goals
- Select goals from Goal Template library
- Group intelligence to narrow down goals templates for team formation

## Participants

- **Voter**: player who is available to work on a team for this cycle.

## Steps

<!--
TODO: update the steps below
- With a modification in that the same goal can be chosen TWICE!
- And the votes being transferred are the ones that didn't get a preference the most (take PGSP into account as to who gets to work on their first choice)
- We also need to calculate the PGSP based on who got which ranked preference.
 -->

1. Determine **open spots**
  - This number determines how many possible teams there are
  - Formula: total no. of voters / TARGET_TEAM_SIZE (round up)
  - Example: 23 / 4 = 6
1. Determine **Droop quota**
  - This number determines the minimum number of votes required for a goal to be selected
  - Formula: (total no. of voters / open spots) + 1
  - Example: (23 / 6) + 1 = 4
1. Vote on goals (build **vote pool**)
  - Each voter receives a 2-position scorecard to vote on their preferred goal template
    - The scorecards have a primary and secondary vote positions
  - Each voter assigns a goal template to each position in their scorecard
    - Voters can choose the same goal template for multiple positions
1. Goal selection (fill **open spots**)
  - Goals whose primary vote count exceeds the Droop quota are selected
  - For each selected goal
    - Determine number of spots to fill
      - Because goals can be chosen by more than one team, the same goal can occupy more than one spot
      - Formula: primary votes for goal / TARGET_TEAM_SIZE (round down)
      - Example: 7 / 4 = 1
    - Fill number of spots with selected goal
    - Determine surplus votes
      - Formula: primary votes for goal % TARGET_TEAM_SIZE
      - Example: 7 % 4 = 3
    - Transfer votes for secondary choice
      - From the set of primary votes for this goal, define the set of goals chosen as a secondary choice
      - For each goal in this set
        - Determine the number of votes to transfer
          - Formula: (number of surplus votes / total number of votes) * number of secondary choices for this goal
          - Example: (3 / 7) * 5 = 2
        - Transfer secondary votes to primary vote for the goal
  - For each unselected goal
    - Transfer votes for secondary choice
      - From the set of primary votes for this goal, define the set of goals chosen as a secondary choice
      - For each goal in this set
        - Determine the number of votes to transfer
          - Formula: (number of surplus votes / total number of votes) * number of secondary choices for this goal
          - Example: (3 / 7) * 5 = 2
        - Transfer secondary votes to primary vote for the goal
  - Repeat until all spots are filled OR there are not enough goals that meet the Droop quota (whichever comes first)
    - If all spots are filled, goal selection is successful
    - If not all spots are filled, goal selection has failed.
      - Start again from "Vote on goals"

<!-- TODO: add an example (w/ diagram) because this algorithm is not easy to understand -->

_Note: this is a modified version of the [Single Transferable Vote](https://en.wikipedia.org/wiki/Single_transferable_vote) process._

## Stats Impacted

None

---

[^1]: Players only vote on goals they want to work on. they don't know they're going to be on team lead until team formation happens. Team leads don't get a formal say in what teams they will be leading, or what they'll be working on when they're team leading.
