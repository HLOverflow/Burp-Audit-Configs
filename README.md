# Burp-Audit-Configs
Targeted vulnerability scanning for burp suite. 

# Problem Statement
Making burp scan every vulnerability for even a single insertion point defined inside Intruder may sometimes take up to 2-3 days! 
In a time constraint environment (ahem... the Portswigger exam...), there is no need to scan all issues in the world. We should only launch specific vulnerability scan in places of suspicion so that the scan complete within minutes instead of hours or days.

Where are custom scanner audit files located? 
`$ ~/.BurpSuite/ConfigLibrary`

# How to use?
1. Add the JSON files to the default Burp directory where audit files are located.
2. Each time you send a request to intruder tab and add an insertion point, right click to get context menu.
3. Choose *Scan defined insertion points > Open Scan Launcher > Scan configuration > Select from library > Custom*

# Observation thus far
Out-of-band detection for various vulnerability class so far has been doing pretty well.

Following are the labs that has been tested on with pretty good detection:
- [Blind OS command injection with out-of-band interaction](https://portswigger.net/web-security/os-command-injection/lab-blind-out-of-band)
- [Blind SQL injection with out-of-band interaction](https://portswigger.net/web-security/sql-injection/blind/lab-out-of-band)

Following are the labs that has performed poorly in detection (targetted scan or just plain scan-all active scan):
- [Blind SQL injection with time delays](https://portswigger.net/web-security/sql-injection/blind/lab-time-delays)
- [Blind SSRF with out-of-band detection](https://portswigger.net/web-security/ssrf/blind/lab-out-of-band-detection)

# TODO
Test the effectiveness of the configuration on more burp labs.
