# Game Terrain

The terrain of our applied game is represented as a map of skills, called the Skills Map.

It currently lives in the [skills-map repository on GitHub][skills-map-repo].

Think of the Skills Map as you would a [trail map][trail-map] or [game map][mario-map]: it shows destinations, paths, and points of interest.

The Skills Map shows learners (and partners, mentors, facilitators, etc.) the missions, exercises, and projects they can complete; what skills are needed to achieve them; how to prove, test, practice, and apply their skills; and which resources are available to help them complete their learning tasks.

Taken together, they chart a grand territory of learnings and offer a map for learners to navigate by with clarity and confidence.

## Legend

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

[skills-map-repo]:https://github.com/LearnersGuild/skills-map
[mario-map]:http://static1.1.sqspcdn.com/static/f/485187/22340105/1364869354830/Mario+World+Map.jpg?token=GREp5UDogM2xw1ImmxH%2FQEjb8Rw%3D
[trail-map]:http://boggsmountain.net/wp-content/uploads/2012/03/BoggsTrailMap2012.jpg
