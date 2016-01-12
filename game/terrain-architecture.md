# Game Terrain Architecture

The terrain of our applied game is represented as a map of skills, called the Skills Map.

It currently lives in the [skills-map repository on GitHub][skills-map-repo].

Think of the Skills Map as you would a [trail map][trail-map] or [game map][mario-map]: it shows destinations, paths, and points of interest.

The Skills Map shows learners (and partners, mentors, facilitators, etc.) the missions, exercises, and projects they can complete; what skills are needed to achieve them; how to prove, test, practice, and apply their skills; and which resources are available to help them complete their learning tasks.

Taken together, they chart a grand territory of learnings and offer a map for learners to navigate by with clarity and confidence.

## Topography

The terrain of the Skills Map is made up of three types of **nodes**:

- [**Projects**](#projects): multi-stage group, pair, or solo work with defined outcomes.
- [**Exercises**](#exercises): simple, short assignments to boost specific capabilities.
- [**Materials**](#materials): useful resources and information, but without any explicit outcome.

These nodes are organized into [**domains**](#domains), or collections of related nodes that build towards particular **skills**.

They may be grouped into sequenced or semi-sequenced clusters called [**missions**](#missions). Missions usually culminate in one large and difficult project.

Learners advance through the terrain by **deploying** projects and working through exercises. Projects and exercises have **objectives** which, when completed, give the learner **skill points** (SP) in one or more **capabilities**.

### Projects

Projects are the most time-intensive nodes of a technical skills map. They may span multiple days or weeks, and may be worked on in pairs or groups as well as alone.

Most projects will have a set of specifications defined that project must adhere to. Some will be very open-ended, letting learners choose their own objectives based on a prompt or within a certain theme.

Example: "Build a Shopify clone that meets these user stories.", "Use a database you've never worked with to create whatever you want."

### Exercises

An exercise is like a tutorial without the explanation part or defined steps. Exercises define clear objectives but do not provide structured steps to achieve them.

Exercises are used to develop habits, build behavior, and to apply and gain knowledge.

Examples: "Write a binary search algorithm that passes a provided test suite.", "Outline endpoints for a RESTful API exposing category, product, and shopping cart resources."

### Materials

Materials are used to build knowledge and beliefs, but are less useful for behavior outcomes.

Seeking and sharing knowledge is a critical part of the learning process, but it is not something that we directly measure.

Materials can be information in one of many forms (text, video, audio, etc.) or a tool that can be used to complete exercises and projects, like a code library or testing framework.

### Domains

Domains are topic-aligned collections of nodes that build towards one or more specific skills.

Learners and pods "explore" and "complete" domains as milestones in their skill training. Think of a domain like a course of learning: it encompasses tasks, projects, and studies, and results in a defined and subject-specific ability.

Examples: "Ruby Land", "Web Apps Mountains", "Mentorship Forest".

### Missions

Missions are sequential or semi-sequential bundles of nodes that frequently culminate in one big group or pair project.

Learners complete missions by working through exercises and deploying projects in a structured order, building up to a difficult final project. In game theory, this missions are akin to "quests" with a final "boss level".

Completing missions gives lots of skill points (SP).

Examples: "Microblogging", "Chat Bot", "Open-Source Expedition".

## Node Attributes

Each node (projects, exercises, materials) has 3 attributes:

- **Title**: descriptive name for the node.
- **Summary**: text summary of the node's purpose and use.
- **Source**: link to an external resource (i.e. the "material" for the node).

For example, an _exercise_ node might look like this:

```
Title: Practice writing basic web servers
Summary: Build a web app that responds to `GET /ping` with a response `pong`. Write two versions of the app, one with Node.js and the other with Ruby. Deploy each app to Heroku or your platform of choice.
Source: http://link.to.online/exercise
```

## Node Relationships

Nodes are _linked_ to each other by different kinds of _paths_ or _relationships_, similar to how sites on a geographic map are linked by roads or trails.

These paths represent relationships of _dependency_ (i.e. a node requires that the learner complete another node) or _support_ (i.e. completing one node will aid the learner to complete another). Other, more nuanced kinds of paths may be discovered as we build out this model.

Paths connect nodes within domains and missions to give learners suggested or mandated courses through the nodes. They also connect domains to each other, showing how learners advance through domains.

For example, within the mission "Web Application Basics" a video on "How a web server works" (material node) might be linked with a _support_ relationship to the tutorial "Deploying to Heroku" (exercise node) and both would be linked with a _dependency_ relationship to the group project "Deploy a web app to remote server".

## Charting a Course

Learners and pods chart their collective and individual courses through the Skills Map to achieve outcomes. Partners, mentors, and facilitators provide suggested courses and also aid learners and pods in charting and navigating their set course.

## Example Terrain Elements

### Mission: Triad Sourcing
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

[skills-map-repo]:https://github.com/LearnersGuild/skills-map
[mario-map]:http://static1.1.sqspcdn.com/static/f/485187/22340105/1364869354830/Mario+World+Map.jpg?token=GREp5UDogM2xw1ImmxH%2FQEjb8Rw%3D
[trail-map]:http://boggsmountain.net/wp-content/uploads/2012/03/BoggsTrailMap2012.jpg
