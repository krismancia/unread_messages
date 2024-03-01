# unread_messages
Write a SQL query to determine which users have more than 10 unread messages.

Select
To_user_id, username
From messages
Join users on users.user_id = messages. To_user_id
Where date_read is null
Group by to_user_id, username
Having count (to_user_id) > 10;
