# Game v.s. Player Support

Our learning OS is expressed through two distinct but related products: Game and Player Support.

The Game includes things like the rules, processes, game mechanics, player stats, and game terrain (challenges). It is meant to challenge the player/learner to demonstrate their capacities, and apply them through play. The better the game, and game terrain are designed, the less player support is needed for learning to happen. A great game stands on its own merits, and is learnable only through play.

Player Support give the player the coaching, resources, tools, environment, practices they need in order to do better at playing the game.

## Karpman Drama Triangle

![Karpman Drama Triangle](http://img.bhs4.com/b6/6/b6636b0849e4d217fc513353f243472bc1aba2b1_large.jpg)

Using the empowerment side of the Karpman Drama Triangle above:

	- Creator = Player
	- Challenger = Game
	- Coach = Player Support

Everything that isn’t part of the *game* is either player support or the player.

The Game is meant to articulate and present the player with a developmental challenge. Player Support helps the player overcome these challenges, and play the game better, faster, healthier, and happier.

## Differentiators


|   | Game Elements | Player Support Elements  |
|---|---|---|
| Challenge v.s. Support | Challenges the player to develop and learn. Reflects their development back to them.  | Supports and coaches the player to meet the challenge. |
| Built by | Game developers releasing new levels, and updating mechanics. And players moding the game | Player Support developers, and potentially player to player support e.g. Learner generated tutorials |
| Variation  | Doesn't change depending on who is playing it and where it's being played  | Changes depending on who is being supported (e.g. black girls edition of LG, v.s. istanbul edition of LG)  |
| Rate of Evolution | Changes and evolves slowly and in serial. Game developers release 1 version at a time and when a change happens it's applied everywhere | Changes rapidly as multiple support implementations try and experiment with better ways to support player in parallel |
| Time Constraints  | Doesn't prescribe when a game is played. Can prescribe how long the game is, or can time bind certain terrain elements  | Prescribes when a player can be supported. Doesn't adjust time boundaries for terrain. |
| Participation  | Permissionless, unconditional participation  | Conditions on acceptance and continued support |
| Absolute needs  | Game cannot be played without these elements  | Game can be played with these elements  |

## Analogies

|   | Game Elements | Player Support Elements  |
|---|---|---|
| Cross Fit  | Crossfit workout of the day, game terrain of different workout practices and strategies, scoring system of tracking reps and time, boundaries of having everything fit into an hour. Dumbells and pull up bars are game objects since you can't play the game without them. | The Gym, the group of people working together, the music, the crossfit coach, the nutritionist, the chiropractor  |
| Chess  | Rules of chess. Chess board and pieces. Chess clock. Tournament rules and scoring |  Chess club. Chess teacher. The North America chess federation. The west coast winter chess tournament |
| Soccer | Rules of soccer. Ball. Field. Notice that the concept of a soccer Team is part of the game, unlike in chess where a chess team is a player support structure. | Referree. Soccer coach. FIFA. Soccer club. Soccer camp. World Cup |


## Software

Both the Game and Player support are expressed and supported through software. It is important to differentiate between the software services that are an expression of the Game mechanics vs. services that are providing Player Support, and when designing these systems, the Game itself should have no dependency on any software that provides Player Support.

### Examples of Game Software

- player collaboration (group chat) software
- scoring and statistics tracking for players and teams
- terrain mapping and traversal

### Examples of Player Support Software

- link-sharing tool (a la reddit)
- financial tracking and planning software (for stipends)

### Loose Coupling

As with any good service-oriented architecture (SOA), services should be loosely coupled. However, some dependencies will exist. For example, the chat software will depend on the single-sign-on (SSO) service. However, it would be a failure of the Game if one of its software services introduced a dependency on a piece of software designed to provide Player Support (for example, if the "terrain traversal" service linked to a resource in the "link-sharing" service). Dependencies in _the other direction_ however, would be okay (e.g., the "link-sharing" service should be able to use the SSO service).


## In Game Player to Player Mentoring

One thing to differentiate and extract here are game mechanics that challenge players to support each other, and develop skills like mentoring and apprenticing. This is distinctly different than player support structures. And is considered part of the game in that they are an essential part of the terrain, and are required to develop, demonstrate and reflect back certain skills, qualities and values.
