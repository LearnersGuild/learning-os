# Statistics

Statistics aggregate information from the [Contract Ledger](game-objects.md).

Their primary purpose is to give feedback to roles, in order to help roles answer questions like:

- What is my current state?
- How am I progressing toward my contract goals?
- Where am I in relation to other people in the system?
- How is the overall system doing?

Statistics, when used correctly, are the fuel that powers learning.

## Aggregate Build Cycles (ABC) [Goal Stat]

The Aggregate Build Cycles for a goal is equivalent to the number of cycles worked on a goal times the size of the team.

Formula: cycles worked on goal X size of team

For example, a goal that takes 2 cycles for a team of 4 has a total of 8 build cycles.

## Assessment Accuracy (AA)

TODO: Flesh out assessment Accuracy

## Build Days (BD) [Player Stat]

Total number of days a player worked on a team in Deliberate Practice as a Team Member or Team Lead. (Build Days = Lead Days + Membership Days)

## Build Cycles (BC) [Player Stat]

Total number of cycles a player worked on a team in Deliberate Practice as a Team Member or Team Lead. (Build Days = Lead Cycles + Membership Cycles)

## Effective Contribution Cycles (ECC) [Player Stat]

An adjustment to a player's BC based on their relative contribution.

The ECC represents a player's effectiveness based on the relative contribution to the total build cycles for a goal.

In the _context of a goal_, the formula for ECC is: RC for goal X ABC for goal.

For example, if after working on a goal with 8 Aggregate Build Cycles, a player with a RC of 32% would have an ECC of 2.56, even though they _technically_ only worked two Build Cycles.

In the _aggregate_, the formula for ECC is: sum of ECC for each goal worked on

For example, if a player has worked on 3 goals and achieved an ECC of 2.2, 3.8, and 0.75 (respectively), their aggregate ECC is 6.75.

## Lead Days (LD) [Player Stat]

Total number of days a player led a team in Deliberate Practice as a Team Lead

## Lead Cycles (LC) [Player Stat]

Total number of cycles a player led a team in Deliberate Practice as a Team Lead

## Effective Lead Cycles (ELC) [Player Stat]

ECC calculated from all cycles completed as a Team Lead.

## Lead to Membership Ratio (LMR) [Player Stat]

Ratio of Lead Cycles to Membership Cycles expressed as a single number.

For example, if a player had 5 Lead Cycles, and 20 Membership Cycles, her ratio would be 1:4, and her LMR would be expressed as 0.25.

## Target LMR [Player Stat]

The ideal ratio of MC to LC, adjusted for effective cycles completed.

Formula: (ECC / (TEAM_LEAD_THRESHOLD * 4)) * 0.25

For example, if Player A has an ECC of 24.6, and the TEAM_LEAD_THRESHOLD is 10 cycles, then Player A's Target LMR is 0.15375.

## Membership Days (MD) [Player Stat]

Total number of days a player joined a team in Deliberate Practice as a Team Member

## Membership Cycles (MC) [Player Stat]

Total number of cycles a player joined a team in Deliberate Practice as a Team Member

## Effective Membership Cycles (EMC) [Player Stat]

ECC calculated from all cycles completed as a Team Member.

## Preferred Goal Selection Percentage (PGSP) [Player Stat]

TODO: update with ranking algorithm
Percentage of time that a player voted for a goal and got assigned to it.

## Relative Contribution (RC) [Player Stat]

The percentage of work contributed by a player to a goal.

Determined in the [retrospective process](../processes/retro.md) by calculating the average of each player on a team's estimation of contribution percentages.

Formula: sum of all contribution estimates for player / team size

For example, if on a 3-player team Player A rates their own contribution at 20%, and the other two players rate Player A's contribution at 40% and 45%, respectively, Player A's RC is 35%.


TODO: cleanup, alphabetize
Minimum EC cycles needed before player can lead. For our purposes it's set at 10 cycles.

TODO: Maybe get rid of build days? Or make Build days what Total contribution is supposed to be
