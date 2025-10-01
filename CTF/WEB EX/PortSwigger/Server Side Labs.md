# Authentication
## Username enumeration via different responses
Go to login page, enter any username and password, catch the request in Burp Proxy, then send to intruder.

In intruder, add payload `$$` to the username field in the request. Paste the username wordlist into the payload list tab. Run a sniper attack on the username, then observe the response. After finding the correct username, do the same for the password. Voila.