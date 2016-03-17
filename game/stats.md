# Documentation: Statistics

Statistics aggregate information from the [Contract Ledger](game-objects.md).

Their primary purpose is to give feedback to roles, in order to help roles answer questions like:

- What is my current state?
- How am I progressing toward my contract goals?
- Where am I in relation to other people in the system?
- How is the overall system doing?

Statistics, when used correctly, are the fuel that powers learning.


<!-- TODO: figure out how stats work -->

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
differential = BD of ranking player - BD of subject player
if differential >= 100, probability is 100
else probability is differential / 100
```

A relevant goal is a goal with a 5 or above relevancy score and at least 50% probability of accuracy.

## Goal Stretchiness Ranking (GSR)

A measure of how stretchy a goal is for a player, i.e. how well the goal sits within the player's PZD.

This answers the question of calibrating appropriate challenges: "will this goal help me advance, but is still within my capacity to accomplish in the allotted time?"

Formula:

```
BD (build days) for goal spent in stretch zone / total BD spent on goal
```

To stay in their PZD, players should aim to keep their GSR as close to 100% as possible.

## Aggregate Relevancy Estimation (ARE)

A measure of goal relevancy across all of a player's goals.

This stat is a composite of two numbers:

- Aggregate relevancy score (mean of all relevancy scores for goals)
- Aggregate probability of accuracy (mean of all probabilities for goals)

## Aggregate Stretchiness Ranking (ASR)

A measure of goal stretchiness across all of a player's goals.

Formula:

```
BD (build days) spent in stretch zone / number of BDs
```
