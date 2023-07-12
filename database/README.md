# README.md - SQLite Database

This database was created in SQLite and manages information related to players, matches, the lobby, and the state of the Tris table. The following tables are included in the database:

1. **Players**: Represents registered players in the system. Each player has a unique ID and a nickname.

2. **Matches**: Represents created matches in the system. Each row represents a match with information such as the match ID, players with their respective scores, and a foreign key reference to the "History_match" table.

3. **Lobby**: Represents the lobby where players join initially to find an online opponent. It is a waiting list with only player IDs.

5. **History_match**: Represents the state of the Tris table during an ongoing game.

![image](https://github.com/bdetoni24/MultiplayerTrisGame/assets/113236784/1fa931c8-de90-47fa-a089-222dbfac536d)


## Table Descriptions

### Players

| Column      | Data Type | Description            |
|-------------|-----------|------------------------|
| player_id   | INTEGER   | Unique player ID       |
| nickname    | TEXT      | Player's nickname      |

### Matches

| Column             | Data Type | Description                                |
|--------------------|-----------|--------------------------------------------|
| match_id           | INTEGER   | Unique match ID                            |
| player1_id         | INTEGER   | Foreign key to player 1                    |
| player2_id         | INTEGER   | Foreign key to player 2                    |
| history_match_id   | INTEGER   | Foreign key to the Tris table state         |
| points_p1          | INTEGER   | Player 1's score                           |
| points_p2          | INTEGER   | Player 2's score                           |

### Lobby

| Column         | Data Type | Description                                  |
|----------------|-----------|----------------------------------------------|
| player_id      | INTEGER   | ID of the player in the lobby                 |

### History_match

| Column         | Data Type | Description                                |
|----------------|-----------|--------------------------------------------|
| history_id     | INTEGER   | Unique history ID of the match              |
| status_cell1   | INTEGER   | Status of cell 1 in the Tris table          |
| status_cell2   | INTEGER   | Status of cell 2 in the Tris table          |
| status_cell3   | INTEGER   | Status of cell 3 in the Tris table          |
| status_cell4   | INTEGER   | Status of cell 4 in the Tris table          |
| status_cell5   | INTEGER   | Status of cell 5 in the Tris table          |
| status_cell6   | INTEGER   | Status of cell 6 in the Tris table          |
| status_cell7   | INTEGER   | Status of cell 7 in the Tris table          |
| status_cell8   | INTEGER   | Status of cell 8 in the Tris table          |
| status_cell9   | INTEGER   | Status of cell 9 in the Tris table          |

In the database, each table is connected through primary and foreign keys, allowing consistent data management and proper relationship between tables. The database has been designed to support future implementations of additional features.
