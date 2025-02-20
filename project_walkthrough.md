<h2>Project Walkthrough</h2>

Login to Splunk:
<img src="https://i.imgur.com/z23MLp6.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/HsTWKt5.jpeg"/>
<br />
<br />

Create a User account for everyone in the team/group:
<img src="https://i.imgur.com/kVpQu65.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/d5F9EUi.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/sSQaJ4g.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/0B7BgfT.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/1h6ESP6.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/KIGi1mz.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/aUPMYwQ.jpeg"/>
<br />
<br />

Changed the timezone to (WAT) and assign roles to the users created, then configured each user to change their password when signed in:
<img src="https://i.imgur.com/C5xDMFp.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/quwPfRH.jpeg"/>
<br />
<br />

All Users Created:
<img src="https://i.imgur.com/Gdaz13z.jpeg"/>
<br />
<br />


 <h2>LOG Analysis</h2>

Next, upload and analyze the logs:

<img src="https://i.imgur.com/2FgzPyD.jpeg"/>
<br />
<br />

Scroll down and select Upload
<img src="https://i.imgur.com/PbCS92b.jpeg"/>
<br />
<br />

Click "Select File"
<img src="https://i.imgur.com/yvnRBNa.jpeg"/>
<br />
<br />

Select "Next" and set the Source Type as "Default"
<img src="https://i.imgur.com/XuOTivT.jpeg"/>
<br />
<br />

Click "Next", leave "Input Settings as "Default" then Review and Submit.
<img src="https://i.imgur.com/Rmx1RM0.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/Nyzedco.jpeg"/>

Select "Start Searching" to begin analyzing the logs
<br />
<br />
<img src="https://i.imgur.com/hTA1xU0.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/hIaOgX4.jpeg"/>
<br />
<br />

Create Dashboard:
<img src="https://i.imgur.com/ZcNKRTj.jpeg"/>
<br />
<br />

Dashboard Created:
<img src="https://i.imgur.com/sY7kmfk.jpeg"/>
<br />
<br />


Create Alerts:
<img src="https://i.imgur.com/kuvcbSr.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/4eCQe2e.jpeg"/>
<br />
<br />
<img src="https://i.imgur.com/eG8iuCJ.jpeg"/>
<br />
<br />

Alert Created:
<img src="https://i.imgur.com/ernHoq4.jpeg"/>
<br />
<br />


Dashboard:
<img src="https://i.imgur.com/wsOVAlr.jpeg"/>
<br />
<br />


 <h2>Findings</h2>

After analyzing the log file, I discovered the log contains multiple failed logins and authentication failures to a remote system. The attacker was trying to connect with a root privilege over an SSH session and most of the SSH requests and Authentication came from a consistent IP:


Failed login request from: 103.99.0.122

Authentication request from: 183.62.140.253


The attacker also tried to log in using the username “user” which wasn’t recognized by the system. The timestamp of the log also signified a brute-force attack that was done
with an automated tool
