# Game Terrain Architecture


## Overview

The terrain of our applied game is represented as a list of Skills, and Quality Rubrics.

Skills are each broken down into Skill Levels.
Each Skill Level defined by an Abilities Set, and a Challenge Set.

The Skill Levels (along with their Abilities Set and Challenge Set) define *what* the player will be engaged in, while the Quality Rubrics defines *how* the player's accomplishments will be evaluated. Quality Rubrics are composed of a Quality Stat, and a Quality Description that spells out how a player's work for that particular challenge is evaluated.

Players traverse the terrain by working on challenges that are available to them for their current skill levels. As they level up, more challenges are unlocked and are available to them.

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

A Challenge belongs to at least 1 or more Skill Levels[^1]. Unless a player has achieved that skill level, they cannot unlock the challenge. The Skill Level section of a challenge, describes which abilities the challenge requires/develops for which Skill level(s), and the Skill Points (SP) associated with each skill level.

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

A Quality Rubric is a Quality Stat, and a Quality Description associated with a certain challenge that determine how a player's work for that particular challenge is evaluated.

For the above challenge, the quality rubrics might look like:

* Completeness: % of objectives that were accomplished
* Code Readability: proper indentation

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

Sprints are the most time-intensive challenges. They may span multiple days or weeks. Sprints tend to be for groups, but can also be for pairs or solo.

Most sprints will have a set of specifications defined that sprint must adhere to. Some will be very open-ended, letting learners choose their own objectives based on a prompt or within a certain theme.

Example: "Build a Shopify clone that meets these user stories.", "Use a database you've never worked with to create whatever you want."

### Project

Projects are smaller than sprints. They can usually be accomplished within 1 day. Projects tend to be for pairs, but can also be solo or group projects.

Example: "Write a Sudoku Solver"

### Drill

A Drill is like a tutorial without the explanation part or defined steps. Drills define clear objectives but do not provide structured steps to achieve them. They can usually be accomplished in under 3 hours. Drills are usually for solo players, but can also be for pairs or groups.

Drills are used to develop habits, build behavior, and to apply and gain knowledge.

Examples: "Write a binary search algorithm that passes a provided test suite.", "Outline endpoints for a RESTful API exposing category, product, and shopping cart resources."

### Level Challenge

A Level Challenge is designed to test/exercises the entire Abilities Set for the *one or more* Skill Levels associated with a Challenge.


## Example Terrain Elements

### Project: How the web works presentation
#### Objectives
* Figure out how the web works
* Present it to your POD in 5 minutes only using a white board

#### Time: 3 hours

#### Players: 3/3

#### Skill Level
** Networking: Level 0 (100 SP)**

Abilities
- can articulate how the internet works

** Presentation: Level 0 (50 SP)**

Abilities
- can present a complex concept to a group

#### Quality Rubrics
* **Completeness:** How complete was your research? How much of it was accurately presented?
* **Work Quality:** How clear was your presentation? How engaging was it?


### Project: 5 week personal goals
#### Objectives
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

#### Time: 1.5 hours

#### Players: 1/1

#### Skill Level
** Networking: Level 0 (100 SP)**

Abilities
- can articulate how the internet works

** Presentation: Level 0 (50 SP)**

Abilities
- can present a complex concept to a group

#### Quality Rubrics
* **Completeness:** How many of the objectives did you attempt/complete?
* **Work Quality:** How brief, actionable, and novel was your work?

### Drill: Self-Documenting Twitter Clone
#### Overview
The objective of this challenge is to write code that is self-documenting in order to create a web-based Twitter clone with the following features:
- Create account
- Sign-in
- Follow / unfollow
- Publish new tweet
- Read recent tweets

#### Objectives
- (25 minutes) Read through the challenge and ensure that both players have a shared understanding of the exercise.
- (90 minutes) Independently code as much of a solution to the problem as you can. Commit frequently.
- (5 minutes) Switch codebases (clone each other’s repositories).
- (90 minutes) Complete the code for the challenge using the other person’s codebase as a starting point.
- (25 minutes) Review each other’s code and score each other in the 3 relevant skill-areas:
- (5 minutes) Score the other player.

#### Time: 4 hours

#### Players: 2/2

#### Skill Level
** Javascript: Level 2 (200 SP)**

Abilities
- can write code that is easily readable by another readable
- can effectively read other people's code and build on it

** Feedback: Level 1 (50 SP)**

#### Quality Rubrics
* **Completeness:** How much of the twitter-clone feature-set did you complete?
* **Code Readability:** How easy was it for your partner to read your code? How easy was it for you to read theirs?

---

[^1]: Challenges cannot belong to multiples Skill Levels *for the same Skill*. For example, a Challenge cannot belong to CSS Level 1 AND CSS Level 2.
