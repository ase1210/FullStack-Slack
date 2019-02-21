`users`

| column name     | data type | details             |
|-----------------|-----------|---------------------|
| `id`            | integer   | primary key         |
| `email`         | string    | not null, unique    |
| `password_digest`| string    | not null            |
| `session_token` | string    | not null, unique    |
| `full_name`      | string    | not null,           |
| `display_name`  | string    |                     |


`chatrooms`

| column name       | data type      | details            |
|-------------------|----------------|--------------------|
| `id`              | integer        | primary key        |
| `name`            | string         | not null, unique   |
| `room_type`       | string         | not null, unique   |
| `admin_id`        | string         | not null, unique   |

`messages`

| column name | data type | details             |
|-------------|-----------|---------------------|
| `id`          | integer   | primary key         |
| `body`        | text      | not null            |
| `author_id`   | integer   | not null, indexed   |
| `message_id`  | integer   | not null, indexed   |

`chatroomUsers`

| column name | data type | details    |
|-------------|-----------|------------|
| `id`          | integer   | primary key         |
| `chatroom_id` | integer   | not null   |
| `user_id`     | integer   | not null   |
| `timestamps`  |           |            |

BONUS
Table name: comments/threads  (can this be part of messages table? )

| column name | data type | details             |
|-------------|-----------|---------------------|
| id          | integer   | primary key         |
| body        | text      | not null            |
| author_id   | integer   | not null, indexed   |
| message_id  | integer   | not null, indexed   |
| timestamps  |           |                     |