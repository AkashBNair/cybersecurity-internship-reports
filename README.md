# Cybersecurity Internship Reports

Lab reports from a 4-week cybersecurity internship at InternPe (22 June 2026 – 19 July 2026).

All work was done in an Oracle VirtualBox lab, with Kali Linux as the attacker machine and Metasploitable2 as the target. Metasploitable2 is an intentionally vulnerable system built for security practice, so the findings below reflect that.

## Reports

| Report | Focus | Tools |
|--------|-------|-------|
| [Week 1: Network Reconnaissance and Traffic Analysis](Week1_Network_Reconnaissance_and_Traffic_Analysis.pdf) | Port and service discovery, packet analysis | Nmap, Wireshark |
| [Week 2: Vulnerability Assessment](Week2_Vulnerability_Assessment_Nessus.pdf) | Vulnerability scan, severity categorisation, mitigations | Nessus Essentials |
| [Week 3: Incident Response (SSH Simulation)](Week3_Incident_Response_SSH_Simulation.pdf) | Simulated unauthorized SSH login attempts, IOCs, root cause analysis | Kali Linux, Nmap, auth.log |

## Summary

**Week 1:** Found 23 open TCP ports on the target. Wireshark captures showed FTP credentials sent in plain text, and I analysed HTTP and FTP traffic and TCP SYN packets. The report includes a threat summary with mitigations.

**Week 2:** A Nessus Essentials basic network scan reported 70 findings, including 4 critical ones (a default VNC password, SSLv2/v3 detection, an end-of-life Ubuntu version, and a bind shell backdoor), with CVSS scores up to 10.0. The report lists mitigations for each finding I documented.

**Week 3:** I simulated unauthorized SSH login attempts by making failed logins from Kali, then found them in the target's authentication logs. The report documents indicators of compromise, a response timeline, root cause analysis, containment actions, and recommendations.

## Notes

- All testing was done in an isolated lab on machines I controlled.
- Each report includes screenshots as evidence.
