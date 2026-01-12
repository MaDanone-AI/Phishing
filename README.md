README: Incident Report PHISH-GROUP-2025-0002
Overview
This repository contains the documentation and analysis for a credential harvesting phishing incident identified as Case ID: PHISH-GROUP-2025-0002. The incident involved a sophisticated impersonation of Microsoft security alerts aimed at stealing user credentials.

Incident Summary

Date Observed: 2025-10-07T09:34:12Z.


Severity: Medium.


Status: Open.


Target: user2@example.com.


Threat Actor Lure: An email claiming the user's Microsoft password had been changed, prompting them to click malicious links to "reset" or "review" security settings.

Key Indicators of Compromise (IOCs)

Sender Domain: msupdate.net (Likely attacker-controlled/typo-squatted).


Sender Address: support@msupdate.net.


Source IP: 77.196.86.10.


Authentication Failures: SPF=fail, DKIM=none, DMARC=none.

Technical Analysis & MITRE ATT&CK
The attack chain involved sending a spoofed email with urgent language to force user execution.


T1566.002: Phishing: Link.


T1598: Phishing for Information.


T1204: User Execution.

Containment & Mitigation

Actions Taken: The email was quarantined, the sender blocked, and the domain submitted for proxy filtering.


Technical Controls: Implementation of strict DMARC policies, URL sandboxing, and browser isolation for high-risk accounts.


Remediation: Enforcement of organization-wide Multi-Factor Authentication (MFA) and automated password resets for impacted users.

Documentation Structure

Executive Summary: High-level overview of the attempt.


Artefacts: Forensic data including raw .eml paths and message headers.


Timeline: Sequence of events from receipt to SOC resolution.


PhishGuard AI Analysis: Automated threat assessment and confidence scoring.
