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
- And the votes being transferred are the ones that didn't get a preference the most (take PGSP into account as to who gets to work on their first preference)
- We also need to calculate the PGSP based on who got which ranked preference.
 -->

1. Determine **open spots**
  - This number determines how many possible teams there are
  - Formula: total no. of voters / MIN_TEAM_SIZE (round up)
  - Example: 23 / 3 = 8
1. Determine **Droop quota**
  - This number determines the minimum number of votes required for a goal to be selected
  - Formula: total no. of voters / open spots (round down) + 1
  - Example: (23 / 8) + 1 = 3
1. Vote on goals (build **vote pool**)
  - Each voter receives a 2-preference scorecard to vote on their preferred goal template
    - The scorecards have a primary and secondary preference
  - Each voter assigns a goal template to each preference in their scorecard
    - Voters can choose the same goal template for multiple preference
1. Goal selection (fill **open spots**)
  - Convert primary preferences to votes for each goal
  - Goals whose vote count exceeds the Droop quota are selected
  - For each selected goal X
    - Assign goal X to one open spot
    - Determine surplus votes
      - Formula: votes for goal X - Droop quota
      - Example: 7 - 3 = 4
    - Transfer surplus votes to secondary preferences
      - From the set of primary preferences for goal X, define the set of goals chosen as a secondary preference
      - For each goal Y in this set
        - Determine the number of surplus votes to transfer
          - Formula: (number of surplus votes / total number of votes for goal X) * number of secondary preferences for goal Y (round to nearest integer)
          - Example: (4 / 7) * 5 = 3
        - Transfer surplus votes to goal Y
    - Recalibrate selected goals (new goals may have exceeded Droop quota after transfer, thus making them selected)
  - If all open spots have been filled, stop process. If not, continue.
  - Pick goal with fewest votes (goal X)
    - Eliminate this goal
    - Transfer votes to secondary preferences in proportion
    - Example: if there are 3 votes for X, and of those votes 2 had secondary preferences for Y and 1 had a secondary preference for Z, then transfer 2 votes to Y and 1 to Z
  - Repeat until all spots are filled
    - If all spots are filled, goal selection is successful
    - If not all spots are filled, goal selection has failed
      - Start again from "Vote on goals"

<!-- TODO: add an example (w/ diagram) because this algorithm is not easy to understand -->

_Note: this is a modified version of the [Single Transferable Vote](https://en.wikipedia.org/wiki/Single_transferable_vote) process._

## Stats Impacted

None

---

[^1]: Players only vote on goals they want to work on. they don't know they're going to be on team lead until team formation happens. Team leads don't get a formal say in what teams they will be leading, or what they'll be working on when they're team leading.
