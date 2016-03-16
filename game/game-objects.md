# Game Objects

## Contract Ledger

A database that tracks contracts, and their state changes.

## Help Request

A request for help. Created with the [requesting help process](./processes.md#requesting-help).

Attributes:

- `Requestors` [type: list of Players, required]
  - Who is requesting help.
- `Helpers` [type: list of Players, defaults to empty]
  - Who responded to the help request.
- `Question` [type: text]
  - Prompt: "What do you need help with? What question do you have that needs answering? Please be as specific as possible."
- `Context` [type: text]
  - Prompt: "Please provide an useful contextual information. For example, a link to the code you're working on, an error message, or a description of why you need this help."
- `Priority` [type: integer, default: 0]
  - Requests start with a 0 priority, which means that they are only visible to players with the same level of experience. The request can get bubbled to players with higher levels of experience if one or more players attempts to help and is unable to resolve it.
- `Created At` [type: timestamp]
  - When the request was created.
- `Resolved At` [type: timestamp, defaults to null value]
  - Whether or not the request has been resolved.

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
  - Whether or not the offering has been accepted.

## Feedback Request

## Feedback Offering
