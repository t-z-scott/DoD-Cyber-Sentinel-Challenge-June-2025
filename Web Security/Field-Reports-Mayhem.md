**Difficulty: Easy**

_Description:_ We've gained access to the Juche Jaguar’s Field Reports archive through an operative's use of weak credentials. Upon logging in, the operative sees their previous field reports and can file new ones. Somewhere in here, I am sure some 'leet' agent stashed the Supreme Leader's secret pizza discount code!

Log in to the portal at: http://35.245.106.190/login.html

Use the credentials: `1234:spudpotato` (`usr:pwd`)

# Completion Steps
1. Login to the URL with the provided credentials.
2. I realized here that this site has an IDOR vulnerability, but I did not use it to solve this challenge.
3. Pick your preferred web content scanner. I'm using [dirb](https://dirb.sourceforge.net/) as my own wordlist did not solve this one.
4. Go to your terminal and run `dirb http://35.245.106.190/`. It should return `/reports`.
5. Navigate to `http://35.245.106.190/reports`, and click `report_GH56IJ.txt`. The flag is in the report text!

> **Flag:** C1{ID0R_F13LD_R3P0RT}

The description mentions a "leet" agent. 1337 is leet-speak for the word leet, and 1337 is the ID for the agent that submitted the correct report. I brute-forced it and still solved it, but this is the *accepted* way to complete it.
