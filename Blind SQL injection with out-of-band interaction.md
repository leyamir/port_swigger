# Background

1. XML, or eXtensible Markup Language, is a **markup language** that defines a set of rules for **encoding documents** in a format that is both **human-readable** and **machine-readable**.
2. Similar to HTML, Markdown
3. Example:
```
<?xml version="1.0" encoding="UTF-8"?>
<note>
  <to>User</to>
  <from>Service</from>
  <heading>Reminder</heading>
  <body>Don't forget the meeting at 3 PM today.</body>
</note>
```
4. Check the respone header to identify if the web application uses XML

### XXE XML External entity 

1. Just a way that **inject** malicious payload to **XML request**, **forces** the server **XML parser** **execute** our malicious code in the injection payload.
2. Create an custom enit --> put it in any tags in XML request --> check if the result appear in the response
```
<!DOCTYPE foo [ <!ENTITY myentity "my entity value" > ]>
<!DOCTYPE foo [ <!ENTITY ext SYSTEM "http://normal-website.com" > ]>
<!DOCTYPE foo [ <!ENTITY ext SYSTEM "file:///path/to/file" > ]>
```
