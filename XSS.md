# Type
1. Relfected XSS
2. Store XSS
3. DOM XSS

- Reflected XSS:
    - Tatics: make attacker's JS code run on victims browser
    - Technique: Create payload and combine it to url of vuln website, send that URL to victim
    - Procedures: use burpsuite, inspect tool, ... to test payload, add payload to URL

# Payload

1. `<img src=1 onerror=alert()>`
2. `" onfocus="alert()`
3. `onload="this.src+=<img src=1 onerror=alert()>`
4. Anything put inside href use this payload `javascript:alert()`
