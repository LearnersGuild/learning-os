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

## Build Cycles (BC) [Player Stat]

Total number of cycles a player worked on a team in Deliberate Practice as a Team Member or Team Lead.

Formula: LC + MC

## Effective Contribution Cycles (ECC) [Player Stat]

An adjustment to a player's BC based on their relative contribution.

The ECC represents a player's effectiveness based on the relative contribution to the total build cycles for a goal.

In the _context of a goal_, the formula for ECC is: RC for goal X ABC for goal.

For example, if after working on a goal with 8 Aggregate Build Cycles, a player with a RC of 32% would have an ECC of 2.56, even though they _technically_ only worked two Build Cycles.

In the _aggregate_, the formula for ECC is: sum of ECC for each goal worked on

For example, if a player has worked on 3 goals and achieved an ECC of 2.2, 3.8, and 0.75 (respectively), their aggregate ECC is 6.75.

## Goal Relevancy Estimation (GRE)

A measure of how relevant a particular goal is for a player.

This answers the question of player orientation and directionality: "will this goal move me in the right direction?"

When choosing a goal, players estimate the relevancy of the goal.

This stat is a composite of two numbers:

- Relevancy score (7-point Likert)
- Probability of accuracy (percent)

The relevancy score is a 7-point Likert rating of the statement: "This goal is relevant to my overarching learning objectives."

The probability of accuracy is a percent representing how confident a player can be that the relevancy score is accurate. This is determined by the experience differential between the player whose goal is being ranked (the subject player) and the player who is ranking (the ranking player). Ranking players with more experience than the subject player will have a higher probability of accuracy, since they have (presumably) more knowledge with which to make an accurate assessment.

Formula for probability of accuracy:

```
differential = ECC of ranking player - ECC of subject player
if differential >= 100, probability is 100
else probability is differential / 100
```

A relevant goal is a goal with a 5 or above relevancy score and at least 50% probability of accuracy.

## Aggregate Relevancy Estimation (ARE)

A measure of goal relevancy across all of a player's goals.

This stat is a composite of two numbers:

- Aggregate relevancy score (mean of all relevancy scores for goals)
- Aggregate probability of accuracy (mean of all probabilities for goals)

## Goal Stretchiness Ranking (GSR)

A measure of how stretchy a goal is for a player, i.e. how well the goal sits within the player's ZPD.

This answers the question of calibrating appropriate challenges: "will this goal help me advance, but is still within my capacity to accomplish in the allotted time?"

Formula:

```
BC for goal spent in stretch zone / total BC spent on goal
```

To stay in their ZPD, players should aim to keep their GSR as close to 100% as possible.

## Aggregate Stretchiness Ranking (ASR)

A measure of goal stretchiness across all of a player's goals.

Formula:

```
BC spent in stretch zone / total BC
```

## Goals Selected (GS) [Player Stat]

The number of goals a player has joined.

## Preferred Goals Selected (PGS) [Player Stat]

The number of goals a player has joined for which the goal was one of their preferences (in the goal selection process).

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

## Lead-Member Contribution Difference (LMCD) [Player Stat]

Within the context of a Team, the LMCD is the difference between a Team Lead's ECC and the mean of all Team Members' ECC.

Formula: Team Lead ECC - MECC

## Mean Effective Contribution Cycles (MECC) [Team Stat]

The mean ECC for all Team Members on a team.

## Membership Cycles (MC) [Player Stat]

Total number of cycles a player joined a team in Deliberate Practice as a Team Member

## Effective Membership Cycles (EMC) [Player Stat]

ECC calculated from all cycles completed as a Team Member.

## Preferred Goal Selection Percentage (PGSP) [Player Stat]

Percentage of time that a player voted for a goal and got assigned to it.

Formula: (PGS / GS) * 100

## Relative Contribution (RC) [Player Stat]

The percentage of work contributed by a player to a goal.

Determined in the [retrospective process](../processes/retro.md) by calculating the average of each player on a team's estimation of contribution percentages.

Formula: sum of all contribution estimates for player / team size

For example, if on a 3-player team Player A rates their own contribution at 20%, and the other two players rate Player A's contribution at 40% and 45%, respectively, Player A's RC is 35%.
