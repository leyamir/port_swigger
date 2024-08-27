# Strategies

- Maybe the csrf token not tied to user session, so attacker can use his own token to change user data
- Cookie editor extension help work with cookie easier

# Payload

- `/?search=test%0d%0aSet-Cookie:%20csrfKey=YOUR-KEY%3b%20SameSite=None` can use to force change stored cookies of victim.
- use <img src=''> tag to load the above payload to set cookie into victim browser
