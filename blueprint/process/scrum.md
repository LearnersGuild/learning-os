# Scrum Process

#### Purpose
Guidelines for harmonious and productive team collaboration.

#### Usage
Follow instructions to best work together with the rest of the LOS team.

---

There are four types of scrum meetings that we use as part of LOS:
- Sprint planning
- Daily standup
- Sprint review
- Retrospective

In addition, there are three roles that take part in the scrum process:
1. Product owner
1. Scrum master
1. Developer

Check out the roles in the [LOS Holacracy circle](https://glassfrog.holacracy.org/circles/6616) for more information.

This document describes the process used in each type of meeting, and how the roles interact.

## Sprint planning
At the beginning of a sprint, we have a planning meeting.

The goal of this meeting is to capture and process new issues, and to develop a work plan for the upcoming sprint.

There are three parts to this meeting. The stages are as follows:

1. **New Issues => Backlog** (all developers, scrum master, and product owner)
  - This stage is complete when all new issues have been moved into the backlog.
  - An issue is ready to move to backlog when it:
    - Has an appropriate tag(s)
    - Is associated with a milestone
    - Has clear success criteria
    - Has an estimate (see "Estimating issues" below)
2. **Prioritization of Backlog** (product owner only)
  - This stage is complete when all of the issues in the backlog have been prioritized.
  - Issues are prioritized by the product owner in the manner that they see fit based on stakeholder input.
3. **Backlog => To Do** (all developers and scrum master)
  - This stage is complete when every developer is clear about what they are working on for this sprint.
  - Each developer picks one or more issue in the backlog and assigns themselves to it.
  - For each issue picked, the developer considers if anything is blocking the issue from being resolved.
    - If yes, then ask: is there an issue capturing that blocking work?
      - If no, create an issue
      - If yes, determine how to resolve that issue first
    - If no, move the issue to To Do

### Estimating issues
Each new issue needs to be assigned an estimate weighting. We use a variation of the Fibonacci scale.

To decide on an estimate weighting, we play **Estimate Poker**.

Each developer decides for themselves what estimate they would apply. We then look at the spread of estimates, and use the mode (most common estimate) for the issue.

To harmonize our respective estimation rubrics, the developers who gave the highest and lowest estimates share their reasoning.

If there is no single mode (i.e. a tie occurs between 2 or more estimates), we play another round until a clear mode is reached.

## Daily standup
Once a day during a sprint, every developer will take < 5 minutes to answer the following questions asynchronously via Slack:

- What work did I do yesterday?
- What am I working on today?
- What blocking issues or impediments might affect my work?

## Sprint review
At the end of a sprint, we do sprint review.

During a sprint review, every developer shares their work from the sprint. At minimum, answer the following questions:

- Which issue(s) did I work on?
- What work did I (and anyone I enlisted to help) produce towards resolving that issue(s)?
- Was my issue accepted by the product owner?
- What blocks did I encounter?

## Retrospective
Not yet implemented.

## Principles Razor (Issue Tests)

When moving an issue into review, make sure to apply the principles razor - the solution should be aligned with our [design principles](../design-principles.md).

By default, all issues should have the razor copied over (via the [issue template](../../.github/ISSUE_TEMPLATE.md)), but it's good to be sure that the ones included in your issue are accurate and up-to-date.
