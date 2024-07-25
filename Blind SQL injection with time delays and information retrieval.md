# Scenario

1. Application uses a tracking cookie and performs a SQL query containing the value of the submitted cookie.
2. Results of the SQL query are not returned, and the application does not respond any differently based on whether the query returns any rows or causes an error.

# Payload

`id=''||(case when('b'='a')then pg_sleep(5)else null end)--`
1. Find way to bruteforce every single character of password of administrator
2. Or there are other way?
