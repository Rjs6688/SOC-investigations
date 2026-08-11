# BRUTE FORCE DETECTION

## Objective

Investigate Windows authentication logs to identify potential brute-force activity, determine the targeted account and source IP address, analyze the authentication timeline, and assess whether the activity resulted in successful access.

## Data Source

Simulated Windows Security Event Logs containing authentication events, including:

* Event ID 4625 – Failed Logon
* Event ID 4624 – Successful Logon

## Investigation Steps

1. Reviewed authentication events for repeated failed login attempts.
2. Identified the targeted user account.
3. Identified the source IP address associated with the failed attempts.
4. Counted the number of failed authentication attempts.
5. Examined the timeline of the authentication events.
6. Checked for a successful login following the failed attempts.
7. Assessed whether the activity was consistent with brute-force behavior.
8. Mapped the observed activity to MITRE ATT&CK.

## Findings

Analysis of the authentication logs identified **10 consecutive failed login attempts** targeting the `administrator` account from the source IP address `185.220.101.45`.

The failed authentication attempts occurred between **09:14:21 and 09:15:24 on 10 August 2026**.

At **09:15:31**, a successful authentication event (Event ID **4624**) was recorded for the same `administrator` account from the same source IP address.

The sequence of multiple failed authentication attempts followed by a successful login within approximately **70 seconds** is consistent with **potential brute-force activity followed by successful authentication**.

Further investigation would be required to determine whether the successful authentication was authorized and whether any subsequent suspicious activity occurred on the affected system.

## Detection Opportunities

A SOC environment could detect similar activity by:

* Monitoring multiple failed authentication attempts from a single source IP.
* Detecting repeated failures against the same user account.
* Alerting when authentication failures occur at a high frequency.
* Correlating multiple failed logins followed by a successful login.
* Monitoring authentication activity involving privileged accounts such as `administrator`.
* Correlating authentication events with endpoint and network telemetry.

## MITRE ATT&CK Mapping

### T1110 – Brute Force

The observed activity is consistent with the **MITRE ATT&CK T1110 – Brute Force** technique because multiple authentication attempts were made against the same account within a short period.

The successful authentication following the failed attempts increases the importance of investigating whether unauthorized access was achieved.

## Recommendations

* Investigate the source IP address `185.220.101.45`.
* Verify whether the successful `administrator` login was authorized.
* Review subsequent activity performed by the account after successful authentication.
* Monitor repeated failed authentication attempts.
* Implement appropriate account lockout or authentication protection policies.
* Enable SIEM alerts for excessive authentication failures.
* Consider restricting or disabling unnecessary use of privileged accounts.
* Correlate authentication logs with endpoint and network events during incident investigation.

## Skills Demonstrated

* Windows Security Event Log Analysis
* Authentication Log Investigation
* Brute Force Detection
* Timeline Analysis
* Security Event ID Analysis
* Threat Detection
* MITRE ATT&CK Mapping
* SOC Investigation
* Incident Analysis

## Investigation Summary

**Target Account:** `administrator`
**Source IP:** `185.220.101.45`
**Failed Attempts:** 10
**Successful Authentication:** Yes
**Successful Event ID:** 4624
**Initial Failed Event ID:** 4625
**Assessment:** Potential Brute-Force Activity

---

> **Note:** The authentication logs used in this investigation are simulated training data created for cybersecurity learning and portfolio purposes.
