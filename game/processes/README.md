# Documentation: Processes

Processes that dictate how players interact with the game.

The most basic processes are those that cover the ways roles interact with contracts, and how contract states change:

- Definition process
- Commitment process
- Engagement process
- Closing process
- Assessment process
- Amendment process
- Voiding process

In addition, there may be specific processes that define how roles interact with each other:

- Feedback process (for roles to give feedback to each other)
- Help request process (for roles to request help from each other)
- ...

In other words, as a player interacting with the LOS, you can only take action via the available processes. They are the rules which govern the system.

A process is defined by three simple attributes:

- Purpose
- Steps
- Results

The purpose explains why this process exists and who can/should use it.
The steps dictate how to execute the process.
The results define what change the process creates.

## Example Process: Requesting Guidance

**Purpose:**<br>
To aid learners in requesting guidance on their learning. In contrast to requesting feedback, which happens _after_ an action is taken, _guidance_ is often needed to help determine _how_ to take action.

**Steps:**<br>
1. Respond to the question: "What do you want guidance on?"
1. Respond to the prompt: "Describe the problem in detail."
1. Respond to the question: "Which options have you considered?"
1. Combine questions/prompts and their responses into one block of text, with lines separating each question/prompt.
1. Post the text to the #guidance-request channel in the LOS chat.

**Results:**
A new guidance request is added to a request queue. This queue is used in the Offering Guidance process.

## Role Processes

### Creating a Role
<!-- TODO: define process -->

### Accepting a Role
<!-- TODO: define process -->

### Revoking a Role
<!-- TODO: define process -->


## Contract Processes

[Cycle](cycle.md)
[Goal Selection](goal-selection.md)
[Project Creation](project-creation.md)
[Retrospective](retro.md)

### Defining a Contract
<!-- TODO: define process -->

### Committing to a Contract
<!-- TODO: define process -->

### Engaging a Contract
<!-- TODO: define process -->

### Closing a Contract
<!-- TODO: define process -->

### Assessing a Contract
<!-- TODO: define process -->

### Amending a Contract
<!-- TODO: define process -->

### Voiding a Contract
<!-- TODO: define process -->


## Requests and Offerings

In the game, there are two types of explicit **requests** and **offerings** that a player can make:

1. _Help_ requests and offerings
1. _Feedback_ requests and offerings

Help can be requested/offered _before an action or decision is taken_ and _during a practice event_.

Feedback can be requested/offered _after an action or decision is taken_ and _after a practice event_.

For example, a team deciding which RSGs to commit to for a cycle may _request help_ from a Mentor. Once they've completed the decision making process, the Mentor may _offer feedback_ on the team's behavior during the decision making process.

### Requesting Help
Any player or team can request help at any time by logging a [help request](./game-objects.md#help-request).

Requesting help contributes to the __ stat of the requesting player/team.

<!-- TODO: determine stats gained for requesting help; players should be incentivized to both request and respond to help requests -->

##### Command

```
/request help <question>
```

Example:

```
/request help "How do I style a table in HTML?"
```

### Offering Help
Any player can offer help by logging a [help offering](./game-objects.md#help-offering).

When offering help, players can either make a _directed_ offer to a particular player or team or a _general_ offer to any player/team who wishes to accept it.

Offering help contributes to the __ stat of the offering player.

<!-- TODO: determine stats gained for offering help; players should be incentivized to offer help -->

##### Command

```
/offer help [<player>...]
```

Examples:

```
/offer help
```

```
/offer help @harry @sally
```

### Requesting Feedback
Any player or team can request feedback at any time by logging a [feedback request](./game-objects.md#feedback-request).

Requesting feedback contributes to the __ stat of the requesting player/team.

<!-- TODO: determine stats gained for requesting feedback; players should be incentivized to both request and respond to feedback requests -->

##### Command

```
/request feedback [<link>] [<message>]
```

Examples:

```
/request feedback https://github.com/sally/mycode/pull/231
```

```
/request feedback "listening skills"
```

```
/request feedback https://github.com/sally/mycode/pull/231 "object-oriented design"
```

### Offering Feedback
Any player can offer feedback by logging a [feedback offering](./game-objects.md#feedback-offering).

When offering feedback, players can either make a _directed_ offer to a particular player or team or a _general_ offer to any player/team who wishes to accept it.

Offering feedback contributes to the __ stat of the offering player.

<!-- TODO: determine stats gained for offering feedback; players should be incentivized to offer feedback -->

##### Command

```
/offer feedback [<topic>] [<player>...]
```

Examples:

```
/offer feedback
```

```
/offer feedback "self-awareness"
```

```
/offer feedback @harry @sally
```

```
/offer feedback "semantic versioning" @harry @sally
```

### Request Bubbling
<!-- TODO: define process -->
