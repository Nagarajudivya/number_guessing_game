# Number Guessing Game

A Bash-based number guessing game that uses PostgreSQL to store player information and game statistics.

## Features

- Generates a random secret number between 1 and 1000.
- Allows users to register with a username.
- Recognizes returning users and displays their game statistics.
- Provides higher or lower hints after each guess.
- Validates user input to accept only integers.
- Tracks the total games played and the best game (fewest guesses).

## Technologies Used

- Bash
- PostgreSQL
- Git

## Database

The `number_guess` database contains a `users` table with the following columns:

- `user_id`: Unique user identifier.
- `username`: Unique username (maximum 22 characters).
- `games_played`: Total number of games played.
- `best_game`: Fewest guesses needed to win.

## How to Run

1. Make sure Bash and PostgreSQL are installed.
2. Create the `number_guess` database and `users` table.
3. Configure the PostgreSQL username in `number_guess.sh`.
4. Give the script executable permission:

   ```bash
   chmod +x number_guess.sh
   ```

5. Run the game:

   ```bash
   ./number_guess.sh
   ```
## Restore Database Backup

To restore the database using the SQL backup:

```bash
psql -U postgres < number_guess.sql
```
