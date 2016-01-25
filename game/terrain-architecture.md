# Game Terrain Architecture

<!-- TOC depthFrom:2 depthTo:4 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Overview](#overview)
- [Skill dependancies](#skill-dependancies)
- [Challenges](#challenges)
	- [Overview (optional)](#overview-optional)
	- [Objective(s)](#objectives)
	- [Skill Level(s)](#skill-levels)
- [Quality Rubric(s)](#quality-rubrics)
- [Time (optional)](#time-optional)
- [Players (optional)](#players-optional)
- [Challenge Types](#challenge-types)
	- [Project](#project)
	- [Drill](#drill)
- [Example Terrain Elements](#example-terrain-elements)
	- [Project: How the web works presentation](#project-how-the-web-works-presentation)
		- [Objectives](#objectives)
		- [Time: 3 hours](#time-3-hours)
		- [Players: 3/3](#players-33)
		- [Skill Level](#skill-level)
		- [Quality Rubrics](#quality-rubrics)
	- [Project: 5 week personal goals](#project-5-week-personal-goals)
		- [Objectives](#objectives)
		- [Time: 1.5 hours](#time-15-hours)
		- [Players: 1/1](#players-11)
		- [Skill Level](#skill-level)
		- [Quality Rubrics](#quality-rubrics)
	- [Drill: Self-Documenting Twitter Clone](#drill-self-documenting-twitter-clone)
		- [Overview](#overview)
		- [Objectives](#objectives)
		- [Time: 4 hours](#time-4-hours)
		- [Players: 2/2](#players-22)
		- [Skill Level](#skill-level)
		- [Quality Rubrics](#quality-rubrics)

<!-- /TOC -->

## Overview

The terrain of our applied game is represented as a list of Skills, and Quality Rubrics.

Skills are each broken down into Skill Levels.
Each Skill Level defined by an Ability Set, and a Challenge Set.

The Skill Levels (along with their Ability Set and Challenge Set) define *what* the player will be engaged in, while the Quality Rubrics defines *how* the player's accomplishments will be evaluated. Quality Rubrics are composed of a Quality Stat, and a Quality Description that spells out how a player's work for that particular challenge is evaluated.

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

A Challenge belongs to at least 1 or more Skill Levels[^1]. The Skill Level section of a challenge, describes which abilities the challenge requires/develops for which Skill level(s), and the Skill Points (SP) associated with each skill level. Challenges within a Skill Level's Challenge Set all contribute SP towards that Skill Level.

For example, the "Build Online Resume" can have the following Skill Levels:

**CSS Level 0 (100 SP)**

Abilities:
- can apply simple responsive design principles

**HTML Level 1 (100 SP)**

Abilities:
- can build a table structure in html without using html tables
- can separate html and css files and link them

### Quality Rubric(s)

A Quality Rubric is a Quality Stat, and a Quality Description associated with a certain challenge that determine how a player's work for that particular challenge is evaluated.

For the above challenge, the quality rubrics might look like:

* Completeness: % of objectives that were accomplished
* Code Readability: proper indentation

### Time (optional)

Some challenges might need to be time bound.

### Players (optional)

Minimum, and Maximum number of players required to attempt this challenge. Some examples:
* 3/5 : this challenge requires at least 3 players, and no more than 5.
* 2/2 : pairs only
* 1/1 : solo players only

## Challenge Types

Challenges can either be Projects, or Drills.

### Project

Projects are the most time-intensive challenges and almost always require a deliverable. They may span multiple days or weeks.

Most Projects will have a set of specifications defined that project must adhere to. Some will be very open-ended, letting learners choose their own objectives based on a prompt or within a certain theme.

Example: "Build a Shopify clone that meets these user stories.", "Use a database you've never worked with to create whatever you want.", "Write a Sudoku Solver"

They can usually be accomplished within 1 day. Projects tend to be for groups or pairs, but can also be solo.


### Drill

A Drill is like a tutorial without the explanation part or defined steps. Drills define clear objectives but do not provide structured steps to achieve them. They can usually be accomplished in under 3 hours. Drills are usually for solo players, but can also be for pairs or groups.

Drills are used to develop habits, build behavior, and to apply and gain knowledge.

Examples: "Write a binary search algorithm that passes a provided test suite.", "Outline endpoints for a RESTful API exposing category, product, and shopping cart resources."

## Challenge Unlocking

All challenges are locked to a player unless:

* They have ALL the skill levels to which a challenge belongs

OR

* They are attempting the challenge as a pair or a group, and *combined* the group has ALL the skill levels to which a challenge belongs.


For example, imagine the following scenario:

*Challenge "Build a twitter clone":* Database Level 3, JavaScript Level 4
*Player A:* Database Level 3, Javascript Level 3
*Player B:* Database Level 0, Javascript Level 5
*Player C:* Database Level 0, Javascript Level 1
*Player D:* Database Level 3, Javascript Level 4

In the above Scenario, only Player D can attempt the "Build a twitter clone" solo.
Players A & B can attempt it as a pair, because combined they have the skill level needed.
Also note that, Player C, can attempt the challenge if they pair with Player D.

### Fungible Skill Points

In the example above, if Player C and Player D pair on the challenge and submit it, they'll both be allocated Database & Javascript Skill Points (SP). Player C will see their SP increase *for the level at which they are*. In other words, unlike abilities sets, SP is not tied to a certain skill level, and is fungible.

## Example Terrain Elements

### Project: How the web works presentation
#### Objectives
* Figure out how the web works
* Present it to your POD in 5 minutes only using a white board

#### Time: 3 hours

#### Players: 3/3

#### Skill Level
**Networking: Level 0 (100 SP)**
- can articulate how the internet works

**Presentation: Level 0 (50 SP)**
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
**Goal Setting: Level 0 (100 SP)**
- can articulate personal goals
- can demonstrate understanding of four quadrants

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
**Javascript: Level 2 (200 SP)**
- can write code that is easily readable by another readable
- can effectively read other people's code and build on it

**Feedback: Level 1 (50 SP)**

#### Quality Rubrics
* **Completeness:** How much of the twitter-clone feature-set did you complete?
* **Code Readability:** How easy was it for your partner to read your code? How easy was it for you to read theirs?

---

[^1]: Challenges cannot belong to multiples Skill Levels *for the same Skill*. For example, a Challenge cannot belong to CSS Level 1 AND CSS Level 2.
