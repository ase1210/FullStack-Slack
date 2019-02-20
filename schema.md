Slack - Features
  Live chat
  Channels
  Direct Message
  Teams or multi-person DM
  Bonus: comments/threads
  Bonus: Search Messages
  Bonus: Notifications


Table name:  users

| column name     | data type | details             |
|-----------------|-----------|---------------------|
| id              | integer   | primary key         |
| email           | string    | null: false, unique |
| password_digest | string    | null: false         |
| session_token   | string    | null: false, unique |
| username        | string    | null: false,        |
| display_name    | string    |                     |
| photo_url       | string    |                     |
| timestamps      |           |                     |

Table name:  chatrooms

| column name       | data type      | details            |
|-------------------|----------------|--------------------|
| id                | integer        | primary key        |
| name              | string         | null:false, unique |
| room_type/channel | string/boolean | null:false, unique |
| timestamps        |                |                    |

Table name: messages

| column name | data type | details             |
|-------------|-----------|---------------------|
| id          | integer   | primary key         |
| body        | text      | null:false          |
| author_id   | integer   | null:false, indexed |
| message_id  | integer   | null:false, indexed |
| timestamps  |           |                     |

Table name: chatroomUsers

| column name | data type | details    |
|-------------|-----------|------------|
| chatroom_id | integer   | null:false |
| user_id     | integer   | null:false |
| timestamps  |           |            |

BONUS
Table name: comments/threads  (can this be part of messages table? )
| column name | data type | details             |
|-------------|-----------|---------------------|
| id          | integer   | primary key         |
| body        | text      | null:false          |
| author_id   | integer   | null:false, indexed |
| message_id  | integer   | null:false, indexed |
| timestamps  |           |                     |