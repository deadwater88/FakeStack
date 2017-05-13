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

### Work_history
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
Company     | string    | not null
Position    | string    |
user_id     | integer   | not null, foreign key (references users), indexed
City/Town   | string    |
Description | text      |
Start Date  |           |
End Date    |           |







## notebooks
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
author_id   | integer   | not null, foreign key (references users), indexed
title       | string    | not null
description | string    |

## tags
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
name        | string    | not null

## taggings
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
note_id     | integer   | not null, foreign key (references notes), indexed, unique [tag_id]
tag_id      | integer   | not null, foreign key (references tags), indexed
