# Schema Information

## users
column name     | data type | details
----------------|-----------|-----------------------
id              | integer   | not null, primary key
username        | string    | not null, indexed, unique
email           | string    | not null, indexed, unique
password_digest | string    | not null
session_token   | string    | not null, indexed, unique

## Profile
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
Biography   | string    | not null
Work_history| text      | string,
user_id     | integer   | not null, foreign key (references users), indexed
Current City| string    | not null,
Relationship| string    |
image_url   | string    |

## Work_history
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
Organization| string    | not null
Position    | string    |
user_id     | integer   | not null, foreign key (references users), indexed
City/Town   | string    |
Description | text      |
Start Date  | Date      |
End Date    | Date      |

## Education_history
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
School      | string    | not null
Graduated   | Boolean   | default true
user_id     | integer   | not null, foreign key (references users), indexed
Type        | string    | high_school, college
City/Town   | string    |
Focus       | text      |
Start Date  | Date      |
End Date    | Date      |


## Comments
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
author_id   | integer   | not null, foreign key (references users), indexed
post_id     | integer   | foreign key (references Posts), indexed
Content     | text      | not null

## Friend_requests
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
requester_id| integer   | not null, foreign key (references users), unique in context of recipient_id
recipient_id| integer   | not null, foreign key (references users)
Approved    | Boolean   | not null, default: false

## Taggings
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
comment_id  | integer   | not null, foreign key (references comments), unique in context of user_id
user_id     | integer   | not null, foreign key (references users), indexed
tagger_id   | integer   | not null, foreign key (references users)

## Posts
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
author_id   | integer   | not null, foreign key (references users), indexed
Content     | text      | not null
