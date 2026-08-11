BRUTE FORCE DETECTION
Objective

Investigate repeated Windows authentication failures to identify potential brute-force activity, determine the targeted account and source IP address, and assess whether a successful login occurred following the failed attempts.

Data Source

Windows Security Event Logs containing authentication events, including failed and successful logon attempts.

Investigation Steps
Review authentication events and identify repeated failed login attempts.
Identify the username targeted during the authentication attempts.
Identify the source IP address associated with the activity.
Analyze the timestamps and frequency of the failed attempts.
Check for a successful authentication following the failed attempts.
Establish a timeline of the suspicious activity.
Determine whether the activity is consistent with a brute-force attack.
Map the observed activity to the relevant MITRE ATT&CK technique.
Findings

To be completed after analysis of the authentication logs.

Detection Opportunities
Detect multiple failed authentication attempts from the same source IP.
Monitor repeated authentication failures against a single account.
Correlate multiple failed logins followed by a successful login.
Configure SIEM alerts for abnormal authentication patterns.
MITRE ATT&CK Mapping

T1110 – Brute Force

The observed authentication activity is assessed against the MITRE ATT&CK Brute Force technique based on the frequency and pattern of authentication attempts.

Recommendations
Monitor repeated failed authentication attempts.
Configure appropriate account lockout or authentication protection policies.
Enable SIEM alerting for excessive authentication failures.
Investigate successful logins following multiple failed attempts.
Review source IP addresses associated with repeated authentication failures.
Skills Demonstrated
Windows Security Event Log Analysis
Authentication Log Investigation
Brute Force Detection
Timeline Analysis
Threat Detection
MITRE ATT&CK Mapping
SOC Investigation
