# Chapter

A group of cohorts that share their skills with each other. Chapters are committed to developing the same craft. Chapter is a game object. Players in the same chapter are committed to each others learning.

# Cohort

A group of players starting at the same location, on the same day. Cohorts can be made up of 1 or more pods. A cohort belongs to one Chapter. They are a game object.

# Craft

A knowledge skill that people need to build things together. Examples: Dot net web developer, IOS developer, android developer, devops, data science, UX design, game development

# Cycle

The primary game loop. Cycles are a game structure (process). Cycles provide a heartbeat, a tick to the game. They are analogous to turns in chess or plays in American football.

Life of a cycle: Goal Selection -> Team Formation -> Deliberate Practice -> Retrospective.

[More on cycles](game/processes/cycle.md).

# Deliberate Practice

Building something in a context that approximates/simulates the "real world" as much as possible with the intention of deliberately practicing the craft.

# Goal

Goals are the core feature for directing learning and collaborative work. They provide structure for teams to form around, and for players to direct their practice.

Goals can be single cycle, or multi-cycle.

A goal is a game structure (contract).

# Guild

A group of chapters. A guild is a game object.

# Human Development

Human Development is the phrase used to refer to the craft-agnostic learning modules and other similar content offered at Learners Guild. The practice of learning Human Development skills at Learners Guild includes the study of four core competencies: meta-learning (learning to learn), self-efficacy, collaboration, and navigating systems.

# Pod

12 to 15 players that are part of the same cohort. Pods are a player support structure.

# Phase

1 phase is 5 weeks. Phases are a player support structure.

# Project

A Project is a Team of players working together on a specific Goal.
One way to think about it, is that a Project is an instance of a Goal created so that a team of Players can attempt it. 

Players work on 1 Project with a Team for 1 or more Cycles.

A project is a game structure (game object).

# Retrospective

End of every cycle
goal progress, relative contribution, professional demand, goal quality, team behavior...etc.

Read about the [Retrospective process](./game/processes/retro.md)

# Stage

1 stage is 10 weeks, or 2 phases. Stages are a player support structure.

A section of the game through which players advance towards victory. Stages correspond to roles; moving a higher stage is analogous to acquiring a role with greater power and responsibility.

# Team

A team is composed of 3 or more players working on a specific Project for one or more cycles. Teams form around a Project when the it begins and dissolve at the end of the project.

Team composition can change in between cycles during multi-cycle projects.

Teams are a game structure (game object).

## Team Member

A Team Member is a player working on a team. Team Members by definition have fewer ECC than their Team Lead.

Team Member is a game mechanic (role).

## Team Lead

A Team Lead is a player leading a team to accomplish a goal. Team Leads by definition have fewer ECC than the mean ECC of their Team Members.

Team Lead is a game mechanic (role).

# Unlearning

Learning is happening all the time, in both functional and dysfunctional ways and is influenced by past experiences of learning, both functional and dysfunctional. Unlearning is to examine the way that one learns, explore what has influenced the ways that one learns, examine the efficacy of the ways that one learns, and discard, or unlearn, those ways that are not effective.

<!-- CONSTANTS -->

# MAX_TEAM_SIZE
5 players

# MIN_TEAM_SIZE
3 players

# TARGET_TEAM_SIZE
4 players

# TEAM_LEAD_THRESHOLD
10 cycles

The number of cycles over the mean of all team members needed to be eligible to lead a team.
