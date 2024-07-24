# Scenario
1. The application uses a tracking cookie and performs a **SQL query** containing the value of the submitted cookie.
2. Results of the SQL query are not returned.
3. The application does not respond any differently based on whether the query returns any rows or causes an error.
4. The query is executed synchronously, it is possible to trigger **conditional time delays** to infer information. 
