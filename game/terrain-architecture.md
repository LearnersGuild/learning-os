# Game Terrain Architecture


## Overview

The terrain of our applied game is represented as a list of Skills, and Quality Rubrics.

Skills are each broken down into Skill Levels.
Each Skill Level defined by an Abilities Set, a Challenge Set.

The Skill Levels (along with their Abilities Set and Challenge Set) define *what* the player will be engaged in, while the Quality Rubrics defines *how* the player's accomplishments will be evaluated. Quality Rubrics are composed of a Quality Stat, and a Quality Description that spells out how a player's work for that particular challenge is evaluated.

Players traverse the terrain by working on challenges that are available to them in for their skill levels. As they level up, more challenges are unlocked and are available to them.

## Skill dependancies

Skill Levels are locked to a player, unless she has achieved its dependancies. A Skill Level dependancies are expressed through other skill levels. Each Skill Level is, by default, dependent on the previous level for that skill.
Skill Levels can also be optionally dependent on another Skill Level. Skill Level 0s that don't have other Level dependancies are automatically unlocked.

For example: Full Stack Dev Level 3, is automatically dependent on Full Stack Dev Level 2, but could also be dependent on Front End Level 2, Database Level 1, and Teamwork Level 1. Meanwhile, SQL Level 0, might not be automatically unlocked, because it depends on Database Level 1.

The Skill Level Dependancies are articulated and expressed through the Skills Map.

## Challenges

Challenges are the main way a player interacts with and plays the game. A challenge is made up of the following elements:
### Overview (optional)

Describes the context, and big picture of the challenge. Sets the stage for the objectives.

Example: "This project is designed to help you to get started with front end css and html skills, while at the same time strengthening your online presence."

### Objective(s)

An Objective is a demonstrable and specific goal for the challenge. Challenges with multiple objectives usually build on each other.

For example, a "Build online Resume" challenge can have these objectives:
- Using only html and css, and no html tables, build an online resume
- Purchase your own domain and host it there
- Apply responsive design principles to your resume

### Skill Level(s)

A Challenge belongs to at least 1 or more skill levels. Unless a player has achieved that skill level, they cannot unlock the challenge. The Skill Level section of a challenge, describes which abilities the challenge requires/develops for which Skill level(s), and the Skill Points (SP) associated with each skill level.

For example, the "Build Online Resume" can have the following Skill Levels:

**CSS Level 0 (100 SP)**
Abilities:
- can apply simple responsive design principles

**HTML Level 1 (100 SP)**
Abilities:
- can build a table structure in html without using html tables
- can separate html and css files and link them

**Web Ops Level 0 (50 SP)**
Abilities
- can purchase & setup domain
- can setup hosting

The above challenge will only be available to players who have leveled up to HTML Level 1.

## Quality Rubric(s)

A Quality Stat, and Quality Description associated with a certain challenge that determine how a player's work for that particular challenge is evaluated.

For the above challenge, the quality rubrics might look like:

Completeness: % of objectives that were accomplished
Code Readability: proper indentation

## Time (optional)

Some challenges might need to be time bound.

##Players (optional)

Minimum, and Maximum number of players required to attempt this challenge. Some examples:
* 3/5 : this challenge requires at least 3 players, and no more than 5.
* 2/2 : pairs only
* 1/1 : solo players only

## Challenge Types

Challenges can either be Sprints, Projects, or Drills.

### Sprints

Sprints are the most time-intensive challenges. They may span multiple days or weeks, and may be worked on in pairs or groups as well as solo.

Most sprints will have a set of specifications defined that sprint must adhere to. Some will be very open-ended, letting learners choose their own objectives based on a prompt or within a certain theme.

Example: "Build a Shopify clone that meets these user stories.", "Use a database you've never worked with to create whatever you want."

### Project

Projects are smaller than sprints. They can usually be accomplished within 1 day. Projects tend to be for pairs, but can also be solo or group projects.

Example: "Write a Sudoku Solver"

### Drill

A Drill is like a tutorial without the explanation part or defined steps. Drills define clear objectives but do not provide structured steps to achieve them.

Drills are used to develop habits, build behavior, and to apply and gain knowledge.

Examples: "Write a binary search algorithm that passes a provided test suite.", "Outline endpoints for a RESTful API exposing category, product, and shopping cart resources."


## Example Terrain Elements

### Mission: Triad Sourcing
#### Overview
#### Objectives
#### Skill Levels
#### Quality Rubrics
#### Time
#### Players

**Overview**
**Objectives**
**Skill Levels**
**Quality Rubrics**
**Time**
**Players**


**Number of players:** 3
**Objective:** 3 player reading and presentation to pod.
**Time:** 3 hour
**XP:** 50
**Scoring:** (presentation will be graded on content, novelty of presentation, etc. pod grades presentation average)

### Mission: Playing Well With Others
**Number of players:** 2
**Objective:** gain points on the “WE” quadrant
Peer program with someone with whom you have had a previous clearing session.

**Pre-requisite:**
I have pair programmed with this player before
I have cleared with this player since pairing with them

**Scoring:**
- Score the experience with your partner
- Get the average score of the quest
  - if the average score of the quest is higher than the previous average from previous quest
    - assign the current average as the final points for the quest
  - if the average score of the quest is lower than the previous average from previous quest
    - Decrease the current average by the delta between the two scores and assign as the final points for the quest

### Mission: 5 week personal goals
**Time:** 1.5 hour
**Number:** solo + pod presentation
**Points:** 100
**Game Play:**
- Review past XP goals for 4 quadrants: Personal, Social, Technical, Systems
- Review points disparity between past goal and present location, and resulting bonus points (see goal-location table)
- Write one paragraph analysis/discussion of past goal and present reality
- Determine XP goals for 4 quadrants for next 5 weeks: Personal, Social, Technical, Systems
- Write a paragraph with strategy for goal realization
- Update personal dashboard with aspirational goal markers
- Present to pod in ‘Launch room’
- Receive feedback
- Defend aspirations and plan for goal realization
- Make changes to goals/dashboard/write up
- Update pod on any changes via slack
- Take first step towards new goals

**Scoring:**
20 points each for:
- Aspiration
- Realism
- Actionable plan
- Brevity
- Novelty

### Mission: Twitter Clone (self-documenting)
**Play Type:** 2 Players, Player vs. Player
**SPs:** 0 (P) / 100 (So) / 100 (T) / 0 (Sy)
**Time Limit:** 4 hours
**Description:**
The objective of this challenge is to write code that is self-documenting in order to create a web-based Twitter clone with the following features:
- Create account
- Sign-in
- Follow / unfollow
- Publish new tweet
- Read recent tweets
**Game Play:**
- (25 minutes) Read through the challenge and ensure that both players have a shared understanding of the exercise.
- (90 minutes) Independently code as much of a solution to the problem as you can. Commit frequently.
- (5 minutes) Switch codebases (clone each other’s repositories).
- (90 minutes) Complete the code for the challenge using the other person’s codebase as a starting point.
- (25 minutes) Review each other’s code and score each other in the 3 relevant skill-areas:
- (5 minutes) Score the other player.
**Scoring:**
- (So)cial points should be based on the quality of the feedback received.
- (T)echnical points should be awarded based on code readability, quality, follow-through on original design, and whether or not the challenge was completed successfully.

### Mission: Booster Shot
**Play Type:** 2 Players (Player + Mentor), Pair vs. Game
**SPs:** 0 (P) / 100 (So) / 200 (T) / 0 (Sy)
**Time Limit:** up to 4 hours
**Description:**
The objective of this challenge is to improve the understanding of a previously-completed challenge. The Player should present the code to the Mentor for a challenge that was either (a) not completed successfully, or (b) completed, but scored poorly. The challenge chosen should have a time limit of no more than 2 hours.
**Game Play:**
- (15-30 minutes) Mentee presents code for challenge to Mentor.
- (60-90 minutes) Player and Mentor create a new branch and refactor, reimplement, and / or complete the challenge together.
- (remaining time) Player redoes original challenge alone, without referring to codebase worked on with Mentor. Mentor then reviews the code.
**Scoring (Player):**
- (So)cial points awarded by Mentor for clarity of code presentation, quality of questions asked during pair programming, and willingness to be coached.
- (T)echnical points awarded by Mentor based on quality and completeness of code for challenge.
**Scoring (Mentor):**
- (So)cial points awarded by Player based on teaching capacity of Mentor, patience, and clarity of communication.
- (T)echnical points awarded to Mentor based on delta in score between the original Player attempt at the challenge and the post-pairing attempt (as a percentage of the delta between original score and total possible score).

### Mission: To-do List
**Number of players:** 1 Player, Player vs. Game
**SPs:** 100 (P) / 0 (So) / 100 (T) / 0 (Sy)
**Time Limit:** 2 hours
**Description:**
The objective of this challenge is to implement a console-based to-do list with the following features:
- Create new task
- Mark task complete
- Save tasks to disk
- Load tasks from disk
**Game Play:** Implement and submit the code.

### Mission: Dragon Boss
**Number of players:** 2
**Objective:** Defend strategy and code for problem x in the face of Dragon (expert coder)
**Time:**  30 mins
**XP:** 250 Dragon awards points
