# Constants

Values that determine game behavior and are constant across the game mechanics.

When using these numbers in other game mechanics, refer to them by their constant name (ALL_CAPS_NO_SPACES), not their actual value.

| Constant Name       | Value | Measured In |
|:--------------------|:------|:------------|
| MAX_TEAM_SIZE       | 5     | players     |
| MIN_TEAM_SIZE       | 3     | players     |
| TARGET_TEAM_SIZE    | 4     | players     |
| TEAM_LEAD_THRESHOLD | 10    | ECC         |

## Explanations

TEAM_LEAD_THRESHOLD is the number of ECC over the mean of all team members needed to be eligible to lead a team.
