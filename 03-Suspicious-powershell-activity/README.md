# SUSPICIOUS POWERSHELL ACTIVITY

## Objective

Investigate PowerShell execution activity to identify potentially suspicious commands, determine the user and process involved, analyze the execution timeline, and assess whether the activity may indicate malicious execution.

## Data Source

Simulated Windows PowerShell and process execution logs created for cybersecurity training and portfolio purposes.

## Investigation Steps

1. Reviewed PowerShell execution events.
2. Identified the user account associated with the activity.
3. Examined the PowerShell command executed.
4. Analyzed command-line parameters for suspicious or encoded content.
5. Reviewed the execution timestamp and process information.
6. Assessed the activity for indicators of malicious PowerShell usage.
7. Mapped the observed behavior to MITRE ATT&CK.
8. Documented findings and recommended security actions.

## Findings

Analysis of the simulated PowerShell activity identified suspicious PowerShell execution involving an encoded command.

The activity was associated with a user account and involved PowerShell being executed with command-line parameters that require further investigation.

The use of encoded or obfuscated PowerShell commands can be associated with attempts to conceal command content and may indicate potentially malicious activity.

The observed activity should be correlated with additional endpoint, authentication, and network telemetry to determine whether the execution was authorized and whether further malicious actions occurred.

## Detection Opportunities

* Monitor PowerShell process creation events.
* Detect PowerShell commands using encoded or obfuscated content.
* Alert on suspicious PowerShell command-line parameters.
* Monitor unusual PowerShell execution by standard user accounts.
* Analyze suspicious parent-child process relationships.
* Correlate PowerShell execution with network connections.
* Correlate PowerShell activity with authentication and endpoint events.

## MITRE ATT&CK Mapping

### T1059.001 – PowerShell

The observed activity involves PowerShell execution and is mapped to **MITRE ATT&CK T1059.001 – PowerShell**.

PowerShell can be used legitimately for administration but is also frequently abused by threat actors for command execution, automation, and post-compromise activity.

### T1027 – Obfuscated/Compressed Files and Information

Encoded or obfuscated PowerShell commands may also be relevant to **T1027 – Obfuscated/Compressed Files and Information** when the technique is used to conceal the content or intent of commands.

## Recommendations

* Enable PowerShell Script Block Logging.
* Enable appropriate PowerShell module and transcription logging where feasible.
* Monitor suspicious PowerShell command-line activity.
* Investigate encoded or obfuscated PowerShell commands.
* Review the parent process that initiated PowerShell.
* Correlate PowerShell activity with network and endpoint telemetry.
* Investigate unusual PowerShell execution from standard user accounts.
* Use SIEM detection rules to identify suspicious PowerShell patterns.

## Skills Demonstrated

* Windows Event Log Analysis
* PowerShell Investigation
* Process Analysis
* Command-Line Analysis
* Threat Detection
* MITRE ATT&CK Mapping
* SOC Investigation
* Incident Analysis

## Investigation Summary

**Activity:** Suspicious PowerShell Execution
**Primary Technique:** T1059.001 – PowerShell
**Potential Supporting Technique:** T1027 – Obfuscated/Compressed Files and Information
**Assessment:** Potentially Suspicious PowerShell Activity

---

> **Note:** The data used in this investigation is simulated training data created for cybersecurity learning and portfolio purposes.
