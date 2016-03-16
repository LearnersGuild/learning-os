# Game Objects

## Contract Ledger

A database that tracks contracts, and their state changes.

## Help Request

A request for help. Created with the [requesting help process](./processes.md#requesting-help).

Attributes:

- `Requestors` [type: list of Players, required]
  - Who is requesting help.
- `Responders` [type: list of Players, defaults to empty]
  - Who responded to the help request.
- `Question` [type: text]
  - Prompt: "What do you need help with? What question do you have that needs answering? Please be as specific as possible."
- `Context` [type: text]
  - Prompt: "Please provide any useful contextual information. For example, a link to the code you're working on, an error message, or a description of why you need this help."
- `Priority` [type: integer, default: 0]
  - Requests start with a 0 priority, which means that they are only visible to players with the same level of experience. The request can get bubbled to players with higher levels of experience if one or more players attempts to help and is unable to resolve it.
- `Created At` [type: timestamp]
  - When the request was created.
- `Resolved At` [type: timestamp, defaults to null value]
  - When the request was accepted (if ever).

## Help Offering

An offering of help. Created with the [offering help process](./processes.md#offering-help).

Attributes:

- `Offerer` [type: Player, required]
  - Who is offering help.
- `Acceptors` [type: list of Players, defaults to empty]
  - Who accepted the help offering.
- `Offering` [type: text]
  - Prompt: "What are you offering help for? What question can you help answer? Please be as specific as possible."
- `Purpose` [type: text]
  - Prompt: "Why is this help useful?"
- `Created At` [type: timestamp]
  - When the offering was created.
- `Accepted At` [type: timestamp, defaults to null value]
  - When the offering was accepted (if ever).

## Feedback Request

A request for feedback. Created with the [requesting feedback process](./processes.md#requesting-feedback).

Attributes:

- `Requestors` [type: list of Players, required]
  - Who is requesting feedback.
- `Responders` [type: list of Players, defaults to empty]
  - Who responded to the feedback request.
- `Feedback Type` [type: multiple selection]
  - Options: "Behavior", "Thinking", "Craft", "Other"
- `Context` [type: text]
  - Prompt: "Please provide any useful contextual information. For example, a description of a decision you made, a link to a pull request, or a skill you're working on."
- `Priority` [type: integer, default: 0]
  - Requests start with a 0 priority, which means that they are only visible to players with the same level of experience. The request can get bubbled to players with higher levels of experience if one or more players attempts to give feedback but the feedback is deemed insufficient by the requestor.
- `Created At` [type: timestamp]
  - When the request was created.
- `Completed At` [type: timestamp, defaults to null value]
  - When the request was completed (if ever).

## Feedback Offering

An offering of feedback. Created with the [offering feedback process](./processes.md#offering-feedback).

Attributes:

- `Offerer` [type: Player, required]
  - Who is offering feedback.
- `Acceptors` [type: list of Players, defaults to empty]
  - Who accepted the feedback offering.
- `Feedback Type` [type: multiple selection]
  - Options: "Behavior", "Thinking", "Craft", "Other"
- `Created At` [type: timestamp]
  - When the offering was created.
- `Accepted At` [type: timestamp, defaults to null value]
  - When the offering was accepted (if ever).
