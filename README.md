# Burp-Audit-Configs
Targeted vulnerability scanning for burp suite. 

# Problem Statement
Making burp scan every vulnerability for even a single insertion point defined inside Intruder may sometimes take up to 2-3 days! 
In a time constraint environment (ahem... the Portswigger exam...), there is no need to scan all issues in the world. We should only launch specific vulnerability scan in places of suspicion so that the scan complete within minutes instead of hours or days.

Where are custom scanner audit files located?
$ ~/.BurpSuite/ConfigLibrary

# Observation thus far
Out-of-band detection for various vulnerability class so far has been doing pretty well.

Following are the labs that has been tested on with pretty good detection:
- [Blind OS command injection with out-of-band interaction](https://portswigger.net/web-security/os-command-injection/lab-blind-out-of-band)
- [Blind SQL injection with out-of-band interaction](https://portswigger.net/web-security/sql-injection/blind/lab-out-of-band)

Following are the labs that has performed poorly in detection:
- [Blind SQL injection with time delays](https://portswigger.net/web-security/sql-injection/blind/lab-time-delays)

# TODO
Test the effectiveness of the configuration on more burp labs.
